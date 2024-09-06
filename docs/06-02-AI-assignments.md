---
stoplight-id: aee4d8f8e8d2f
---


### When is the AI fine-tuned enough?

You can decide when you are satisfied with fine-tuning. We recommend using a combination of a qualitative check and consulting the AI score to make this decision.

<!-- theme: info -->
> As a rule of thumb, we often recommend to review about 20% of the rows but not more than 300, whichever is lower.

### AI Score

The AI score indicates how indicates **how confident the AI is in its topic assignments.**

#### What is a good score?

The theoretical maximum score is 100, but this is never reached. A few benchmarks:

* We had the same person (a coding professional) manually assign topics to all rows of a project **twice**. She achieved an overlap of the two iterations of around 90.
* When two different people manually assign topics to the same survey, they usually achieve an overlap score in the 70s to 80s, but sometimes it drops even to 60 when there are overlapping topics or ambiguity in the rows.
* When aiming for *"human-level"* performance, it makes sense to aim at a score in the 70s. However, for many applications (such as getting a reliable distribution), a lower score is already sufficient – given there are enough samples.
* A naive model that just randomly guesses, achieves an AI score of around 4 or 5, **not 50**. 

#### Why is there no score for some topics?

If a topic appears only in very few samples, we might not be able to compute a score for this topic. It could also mean the AI didn't understand the topic at all, although this is not very common.

#### Why don't you state the accuracy measure?

For text classification, accuracy is often not a very good measure. If datasets are unbalanced, which is almost always the case when assigning topics to texts (topics usually are *not present* at a much higher rate than *being* present), the accuracy would almost always be ridiculously high (above 98%), but not meaningful.

#### How do you measure the score?

Under the hood, the model does not only assign topics to the rows, but it also forcast a certainty measure for those predictions. We can estimate the AI score starting from such certainty measures.

Technically speaking the score represents the weighted F1 over all topics.


#### How do I get to a higher score?

Before focusing purely on the score, be sure to also check the topic assignments for a few rows qualitatively. Sometimes even a low numeric score can still lead to qualitatively good results. To improve the score, there are a few strategies:

* **Streamline your topic collection:** A very large number of topics is more difficult to assign than when having fewer. As humans would, the AI will also make more mistakes distinguishing between similar / not well differentiated topics.
* **Optimize topic labels:** The AI takes the topic & category labels into account. Therefore, make sure the topic labels are meaningful and not too abstract.
* **Review more rows:** The more examples the AI has to learn from, the better it will become. If you have "historical" data which already has topics assigned but is not uploaded to Caplena yet, contact [support](support@caplena.com) to help you ingest that into your account.

For enterprise customers we are also happy to have one of our language specialists look into your data, just contact [support](support@caplena.com).

#### How is the first score calculated and how can it be calculated without any involvement of a human?

The AI score is an estimate of the model performance on a text to analyze column. To be precise we want to estimate the F1 score. 

To compute the F1 score exactly one would need to have a “ground truth” to which compare the AI prediction. However, this would make the AI prediction useless. Thus the challenge is to make an estimate of the model accuracy without looking at labels.

To make such estimate we exploit the fact that, under the hood, our AI does not output a binary prediction, but rather a certainty measure. Experiments on our data suggest that our model is well [calibrated](https://en.wikipedia.org/wiki/Probabilistic_classification#Probability_calibration), guaranteeing that among all of those predictions where the model has a confidence of `c` roughly the ratio of them which will be picked by a person is `c`. 

A well calibrated model allows to compute the expected value of the number of true positive, false positives and false negatives. Thus allowing us to estimate the weighted F1 score. A more detailed description of the algorithm is at the end of this document.

#### How can one trust that this is correct?

It is impossible to have a guarantee that the F1 score is accurate. People could have a specific way of assigning topics that does not match the confidence of the model. Or the data itself might be so unusual (out of distribution) that the model appears confident even if it is wrong, since it has never seen similar data during the training. However, experiments with data from all our customers show that our prediction is usually spot-on. The cases where we overestimate the AI score by more than 10 points (critical error) are rare; less than 1%.

#### Why and how does reviewing the categorizations lead to changes to the AI Score? 

There are two reasons:

* We consider reviewed rows of text as being correct. For instance, if all rows would be reviewed, you would achieve an AI score of 100. However, if only 1% of the rows are reviewed this would not be very impactful.
* Through the human reviews the model will be fine-tuned, and predictions will run on this basis, yielding a different, ideally a better and better, AI score. This is particularly the case when the reviews are done correctly and consistently. The model will understand the context better and better, resulting in a higher confidence level in its predictions, thus yielding higher AI score.

#### Why don’t we use the human reviews to compute AI score?

This is what we were doing in the past. While this seems to be the most natural thing to do, there are some important drawbacks.
* After reviewing we fine-tune the model on the reviewed data. Thus, we would of course see a very high alignment between the humanly reviewed data and the fine-tuned AI data. However, this would not be representative of the real performance. To address this bias, we would need to split the reviewed data in training and validation. However, if the validation set is large, we are wasting a lot of data for training, but if it was too small a set, we would get an imprecise AI score.
* In “focus mode” you are specifically reviewing rows that are most challenging for the AI. Therefore, after reviewing we will not have a representative sample of the full dataset. In the past we would address this issue making a regression to estimate the F1 score also in the not reviewed rows. Experiments show that our new approach is superior and more precise. Furthermore, this needed a large number of rows to be reviewed to give a first estimate of the AI score, even though, in most instances, it was not needed.



# AI Topic Assignments

![Topic Assignments](images/ai-topic-assignments.png)

Caplena's AI automatically assigns the appropriate topics from your topic-tree to your texts 🪄.

* [How the AI works](#how-the-ai-works)
* [Fine-Tuning](#fine-tuning)

## How the AI works

For a detailed report on the our AI, please download [our whitepaper](https://storage.googleapis.com/caplena-public/Whitepaper_Unveiling_the_tech_behind_the_worlds_most_accurate_customer_feedback_analysis_ai.pdf).

### Understanding of Topics

The AI does *not* work like a keyword matching algorithm. Instead, it attempts to *understand* the topics. This means you don't have to add any synonyms, it already knows that `Overpriced` and `Too expensive` mean the same thing.
See [topic properties](03-01-Topics.md#topic-properties) to understand which topic properties are relevant for the AI.

For sentiment-enabled topics, only *one sentiment version* is assigned at the time, i.e. a row cannot have the `positive` and `negative` version of a topic at the same time.

### Model Architecture

This is of course part of our secret sauce and nothing we can share publicly 🙊. What we can say is that we make use of a heavily modified Transformer architecture. For the technically interested, check out [this article](https://jalammar.github.io/illustrated-transformer/) on transformers.

Technically speaking, the AI performs a multilabel classification, meaning that zero, one or multiple topics can be assigned to the same row.

### AI Training

Our AI is trained in a three-step process:

1. **Pretraining:** First we pretrain it on a massive amount of unstructured data, basically a dump of the internet. From this the AI learns a basic language understanding including things like synonyms, antonyms, and negations.
2. **Training on Caplena's data:** The second, crucial step is to train it on the millions of rows of hand-reviewed data that we have on Caplena.
3. ***(Optional)* Fine-tuning:** Finally, you can fine-tune the AI on a small amount of your specific data, to nudge it into the right direction.

<!-- theme: success -->
> The recommended way to go about this is by using the **Focus Mode 🤓**. Alternatively you can also click on a specific row you want to edit, which will open the sidebar.

See [this article](06-02-AI-assignments.md) to learn more about how the AI assigns topics.

<!-- theme: info -->

> #### By training on my data, will the AI expose information to other users?
>
> The short answer is no. The long one *below*.
>
> We use the *tagged data* on our platform to train our machine learning model. This will not in any way share your data with other users: What the AI learns is the **association of topics with text**, e.g. that `The package arrived late` matches the tag `Slow delivery`. Learning on millions of text comments from our hundreds of customers, the AI gathers these *relations* from the data. These learnings are stored in such an abstracted fashion (not as text, but as matrices of weights in a neural network), that no inference can be made whatsoever on the input data which was used to train this model, even if the model was public. Which it is not, customers only get the *result* of the topic assignments. 

## Fine-Tuning

To fine-tune the AI on your specific data, simply review a sample of your data. Reviewing means going over the rows and either confirming the AI's assignments or changing them to meet your preference. See [this article](06-01-Fine-tuning-view.md#fine-tuning) on how this works in detail.
