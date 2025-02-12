---
stoplight-id: aee4d8f8e8d2f
---

# AI Topic Assignments

![Screenshot 2024-12-04 at 17.21.11.png](<../assets/images/Screenshot 2024-12-04 at 17.21.11.png>)


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


<!-- theme: info -->

> #### By training on my data, will the AI expose information to other users?
>
> The short answer is no. The long one *below*.
>
> We use the *tagged data* on our platform to train our machine learning model. This will not in any way share your data with other users: What the AI learns is the **association of topics with text**, e.g. that `The package arrived late` matches the tag `Slow delivery`. Learning on millions of text comments from our hundreds of customers, the AI gathers these *relations* from the data. These learnings are stored in such an abstracted fashion (not as text, but as matrices of weights in a neural network), that no inference can be made whatsoever on the input data which was used to train this model, even if the model was public. Which it is not, customers only get the *result* of the topic assignments. 

## Managing AI Updates 

Caplena now offers a toggle in the Topics view to control AI updates. This allows you to pause AI learning while still letting the system assign topics automatically when new data is uploaded. It ensures consistency in topic assignments without unexpected AI-driven changes.

### How to Enable or Disable AI Updates:

1️⃣ Navigate to the Topics view in your project.

2️⃣ Click the three-dot menu in the top-right corner.

3️⃣ In the Settings pop-up, find the "AI Updates" toggle (highlighted in the image below).

4️⃣ Turn OFF to pause AI training.

5️⃣ Turn ON to let AI learn from manual reviews again.


![Screenshot 2025-02-12 at 10.55.41.png](<../assets/images/Screenshot 2025-02-12 at 10.55.41.png>)

### What Does This Setting Do?

**AI Updates Disabled:**

❌ Caplena stops learning from manual reviews and topic edits.

✔️ Inference remains active—new data will still get topics assigned based on the existing AI model.

✔️ AI scores remain unchanged, keeping the model stable.


## Fine-Tuning

To fine-tune the AI on your specific data, simply review a sample of your data. Reviewing means going over the rows and either confirming the AI's assignments or changing them to meet your preference. See [this article](06-01-Fine-tuning-view.md#fine-tuning) on how this works in detail.
