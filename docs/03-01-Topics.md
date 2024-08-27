---
stoplight-id: 136b79897741e
---

# Main Concepts

* [Categories](#categories)
* [Topics](#topics)
* [Sentiment](#sentiment)

## Category

A category is a set of topics which are referring to the same overarching theme. A category could be for example `Customer Service`.

*The category is AI-relevant 🤖*.

![Screenshot 2024-08-27 at 15.17.16.png](<../assets/images/Screenshot 2024-08-27 at 15.17.16.png>)

<!-- theme: info -->

> ***AI-relevant 🤖** means the property is considered by the AI during training and when assigning topics.


## Topic

**Topics**, also known as *codes, themes, classes or labels* by some, summarize what is mentioned in your text comments.
![Screenshot 2024-08-27 at 15.20.34.png](<../assets/images/Screenshot 2024-08-27 at 15.20.34.png>)

### Topic Label

Concise meaning of the topic. This is what's displayed on the topic chips and is used by our AI to assign topics to texts. A good topic name should be short while still conveying the meaning of the topic in plain text. Examples for topic names are `Staff friendliness` or `Shipping Fees`.

*The label is AI-relevant 🤖*.

### Topic Sentiment
Sentiment refers to whether responses in your project are positive, negative, or neutral. This is often used in projects like NPS studies or any other survey where feedback can range from positive to negative.

For instance, in customer feedback, Caplena might identify topics like "customer service," "product quality," and "pricing." The sentiment analysis then evaluates whether the feedback on each topic is positive, negative, or neutral. This helps you understand not just the overall sentiment but also how each aspect of your product or service is perceived by customers.



| Positive | Neutral  | Negative  |
|---|---|---|
| <img src="https://raw.github.com/caplena/knowledge-base/master/docs/images/topic_positive.png" style="width:170px;"/> | <img src="https://raw.github.com/caplena/knowledge-base/master/docs/images/topic_neutral.png" style="width:170px;"/> |  <img src="https://raw.github.com/caplena/knowledge-base/master/docs/images/topic_negative.png" style="width:170px;"/> |

This means you must only create **one** topic for all three sentiment attitudes from - the AI will then automatically assign the correct one.

<!-- theme: info -->

> Note: It is completely optional to enable sentiment on topics, you can also continue to use them without sentiment.

<div style="display:flex; align-items: center">
<div>Codes without sentiment don't have any indicator:</div>
<img src="https://raw.github.com/caplena/knowledge-base/master/docs/images/topic_no_code.png" style="width:100px;"/>
</div>

<!-- theme: warning -->
> #### Enabling topic sentiment
>
> The sentiment can only be enabled for topics **without any reviewed rows**. 
>
> Note: **Merging** multiple non-sentiment topics into a sentiment topics is always possible, even with reviewed rows. Below you´ll find a video that outlines how to do that:
>
> https://www.youtube.com/watch?v=Fma9N8cNi78
> When activated, the AI will start differentiating between the sentiment versions.

<!-- theme: warning -->
> #### Disabling topic sentiment
>
> When disabling the topic sentiment, the sentiment will be discarded from the topic in all rows. **This action is non-reversible**.

### Topic Properties

Topics have slightly different properties, depending on if *topic sentiment* is enabled or not:

| *With* topic sentiment | *Without* topic sentiment |
|---|---|
| <img src="https://raw.github.com/caplena/knowledge-base/master/docs/images/topic_with_sentiment.png" style="width:330px;"/> | <img src="https://raw.github.com/caplena/knowledge-base/master/docs/images/topic_wo_sentiment.png" style="width:330px;"/> |



### Sentiment Labels

Optional sentiment-specific topic labels, which are displayed on topic chips and charts instead of the topic label   itself. 
*Example:* `Friendly` / `Unfriendly` for topic name `Friendliness`. <br>Only available if topic-sentiment is enabled.

*The sentiment labels are AI-relevant 🤖*.

### Code

Unique numerical identifier for a specific topic and its sentiment. This can be used to visualize and compare across studies or to trigger predefined actions based on the assigned topic and its sentiment. You can choose the code if you want to, otherwise we automatically assign one.

### Description

Longer description of the topic for reference. This field is not used by our AI to assign the topic, therefore make sure that the essence of the description is contained in the topic label & category.


### Keywords

Keywords are not available by default, as our AI is designed to **learn from examples rather than rules**. This is a much more efficient process than defining various synonyms manually as keywords.

However, if you have a use-case which justifies the usage of keywords, our support can enable them for you. Please note that when enabled, keywords behave as **exact matches**.

<!-- theme: info -->

> Example: The keyword `we` would match the word `however`. You should therefore limit yourself to very few, specific keywords, that the AI couldn't pick up otherwise.

An additional feature of keywords are *regular expressions* (or regexes): You may add these kinds of expressions to a keyword within slashes, to look for specific character combinations. 

<!-- theme: info -->

> Example: The keyword `/[0-9 ]{6,10}/` would match rows that contain a consecutive sequence of 6-10 digits or whitespaces and could be a primitive template for finding phone numbers.
>
> *Note: This would also match a row with only 6 consecutive whitespaces.*



