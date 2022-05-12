# AI Topic Assignments

![Topic Assignments](images/ai-topic-assignments.png)

Caplena's AI automatically assigns the appropriate topics from your topic-tree to your texts 🪄.

* [How the AI works](#how-the-ai-works)
* [Fine-Tuning](#fine-tuning)
  * [Focus Mode](#focus-mode)
  * [When is the AI updated?](#when-is-the-ai-updated)
  * [When is the AI fine-tuned enough?](#when-is-the-ai-fine-tuned-enough)
  * [AI Score](#ai-score)

## How the AI works

### Understanding of Topics

The AI does *not* work like a keyword matching algorithm. Instead it tries to *understand* the topics. This means you don't have to add a lot of synonyms, it already knows that `Overpriced` and `Too expensive` mean the same thing.
See [Topic Properties](docs/02-01-Topics.md#topic-properties) to understand which topic properties are relevant for the AI.

### Model Architecture

This is of course part of our secret sauce and nothing we can share publicliy 🙊. What we can say is that we make use of a heavily modified Transformer architecture. For the technically interested, check out [this article](https://jalammar.github.io/illustrated-transformer/) on transformers.

### AI Training

Our AI is trained in a three step process:

1. **Pretraining:** First we pretrain it on a massive amount of unstructured data, basically a dump of the internet. From this the AI learns a basic language understanding including things like synonyms, antonyms and negations.
2. **Training on Caplena's data:** The second, crucial step is to train it on the millions of rows of hand-reviewed data that we have on Caplena.
3. ***(Optional)* Fine-tuning:** Finally you can fine-tune the AI on a small amount of your specific data, to nudge it into the right direction.

## Fine-Tuning

To fine-tune the AI on your specific data, simply review a sample of your data. Reviewing means going over the rows and either confirming the AI's assignments or changing them to meet your preference. See [TODO]

### Focus Mode

The most efficient way to fine-tune your data is by activating the focus mode 🤓. This mode does a couple of things:
* Sort the rows by **AI certainty**: This means that you will first be shown the texts where the AI ist *most unsure* on its assignments. By reviewing and potentially correcting these assignments first, the AI is learns much more efficiently.<br>This technique is also known as *active learning*.
* Filter for non-reviewed rows only, as you do not want to look at these rows again.
* Hide any potential distractions, so you can fully focus on the current row you're looking at.

### When is the AI updated?

#### 1. After enough Reviews

As you review rows, a counter will indicate when the next AI update will be triggered. The first update happens after 20 reviews, the second after 50, then 100 and so on.

The "distance" between updates gets larger as trainings become more computationally expensive and the incremental amount of information gained from a review decreases with the amount of data.

*Note:* Bulk assigments [TODO] only count as a single review.

![AI Update](images/ai-next-update.png)


#### 2. When changing Topics

If any of the [AI-relevant topic properties](docs/02-01-Topics.md#topic-properties) are changed, the AI will be fine-tuned again. In some cases a delay of 30-60 seconds is applied before starting the update.

### When is the AI fine-tuned enough?

You can decide when you are satisfied with fine-tuning. We recommend using a combination of a qualitative check and consulting the AI score to make this decision.

<!-- theme: info -->
> As a rule of thumb we often recommend to review about 20% of the rows but not more than 300, whichever is lower.

### AI Score

The AI score indicates how well **your reviewed topic assignments match the AI's auto-assigments.** For the score to become available, you need to have reviewed at least 50 rows.

#### What is a good score?

The theoretical maximum score is 100, but this is never reached. A few benchmarks:

* We had the same person (a coding professional) manually assign topics to all rows of a project **twice**. She achieved an overlap of the two iterations of around 90.
* When two different people manually assign topics to the same survey, they usually achieve an overlap score in the 70s to 80s.
* When aiming for *"human-level"* performance, it makes sense to aim at a score in the 70s. However, for many applications (such as getting a reliable distribution), a lower score is already sufficient – given there are enough samples.

#### Why is there no score for some topics?

If a topic appears only in very few samples, we might not be able to compute a score for this topic. It could also mean the AI didn't understand the topic at all, although this is not very common.

#### Why don't you state the accuracy measure?

For text classification, accuracy is often not a very good measure. If datasets are unbalanced, which is almost always the case when assigning topics to texts (topics usually are *not present* at a much higher rate than *being* present), the accuracy would almost always be ridiculously high (above 98%), but not meaningful.

#### How do you measure the score?

When training our machine learning model, we leave out a part of the data you have reviewed. Scoring is then done on the left out data.

Technically speaking the score represents the weighted F1 over all topics.


#### How do I get to a higher score?

Before focusing purely on the score, be sure to also check the topic assignments for a few rows qualitatively. Sometimes even a low numeric score can still lead to qualitatively good results. To improve the score, there are a few strategies:

* **Streamline your topic tree:** A very large number of topics is more difficult to learn than when having fewer. As humans would, the AI will also make more mistakes distinguishing between similar / not well differentiated topics.
* **Optimize topic labels:** The AI takes the topic & category labels into account. Therefore, make sure the topic labels are meaningful and not too abstract.
* **Review more rows:** The more examples the AI has to learn from, the better it will become. If you have "historical" data which already has topics assigned but is not uploaded to Caplena yet, contact support to help you ingest that into your account.

For enterprise customers we are also happy to have one of our language specialists look into your data, just contact support.
