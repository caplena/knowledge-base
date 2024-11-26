---
stoplight-id: 136b79897741e
---

# Main Concepts

* [Category](#category)
* [Topic](#topic)
* [Topic Sentiment](#topic-sentiment)

## Category 

A category is a set of topics which are referring to the same overarching theme. A category could be for example `Features`.

![Screenshot 2024-11-19 at 17.14.21.png](<../assets/images/Screenshot 2024-11-19 at 17-2.14.21.png>)



*The category is AI-relevant 🤖*.



<!-- theme: info -->

> ***AI-relevant 🤖** means the property is considered by the AI during training and when assigning topics.


## Topic

**Topics**, also known as *codes, themes, classes or labels* by some, summarize what is mentioned in your text comments.

![Screenshot 2024-11-19 at 17.15.49.png](<../assets/images/Screenshot 2024-11-19 at 17.15.49.png>)


### Topic Label

Concise meaning of the topic. This is what's displayed on the topic chips and is used by our AI to assign topics to texts. A good topic name should be short while still conveying the meaning of the topic in plain text. Examples for topic names are `Staff friendliness` or `Shipping Fees`.

*The label is AI-relevant 🤖*.

## Topic Sentiment
Sentiment refers to whether responses in your project are positive, negative, or neutral. This is often used in projects like NPS studies or any other survey where feedback can range from positive to negative.

For instance, in customer feedback, Caplena might identify topics like "customer service," "product quality," and "pricing." The sentiment analysis then evaluates whether the feedback on each topic is positive, negative, or neutral. This helps you understand not just the overall sentiment but also how each aspect of your product or service is perceived by customers.

![Screenshot 2024-11-19 at 17.18.57.png](<../assets/images/Screenshot 2024-11-19 at 17.18.57.png>)


This means you must only create **one** topic for all three sentiment attitudes from - the AI will then automatically assign the correct one.

<!-- theme: info -->

> Note: It is completely optional to enable sentiment on topics, you can also continue to use them without sentiment.

<div style="display:flex; align-items: center">
<div>Codes without sentiment don't have any indicator:</div>
<img src="https://raw.github.com/caplena/knowledge-base/master/docs/images/topic_no_code.png" style="width:100px;"/>
</div>
<!-- theme: warning -->



### Topic Properties

Topics have slightly different properties, depending on if *topic sentiment* is enabled or not:

![Screenshot 2024-11-19 at 17.59.20.png](<../assets/images/Screenshot 2024-11-19 at 17.59.20.png>)



### Sentiment Labels

Optional sentiment-specific topic labels, which are displayed on topic chips and charts instead of the topic label   itself. 
*Example:* `Friendly` / `Unfriendly` for topic name `Friendliness`. <br>Only available if topic-sentiment is enabled.

*The sentiment labels are AI-relevant 🤖*.

### Code

Unique numerical identifier for a specific topic and its sentiment. This can be used to visualize and compare across studies or to trigger predefined actions based on the assigned topic and its sentiment. You can choose the code if you want to, otherwise we automatically assign one.

### Description

Longer description of the topic for reference. This field is not used by our AI to assign the topic, therefore make sure that the essence of the description is contained in the topic label & category.


