# Sentiment Topics

* [Overview](#overview)
* [Topic Properties](#topic-properties)


*Check out the [🚀 Migration Guide](02-01-Migration-guide.md) to learn how to convert existing projects to make use of sentiment topics.* 

## Overview

**Topics**, also known as *codes, themes, classes or labels* by some, summarize what is mentioned in your text comments. Topics can have different sentiments:

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

## Topic Properties

Topics have slightly different properties, depending on if *topic sentiment* is enabled or not:

| *With* topic sentiment | *Without* topic sentiment |
|---|---|
| <img src="https://raw.github.com/caplena/knowledge-base/master/docs/images/topic_with_sentiment.png" style="width:330px;"/> | <img src="https://raw.github.com/caplena/knowledge-base/master/docs/images/topic_wo_sentiment.png" style="width:330px;"/> |

Property | New in v2 | AI relevant 🤖* | Meaning 
---------|----------|---------|---------
| **[Label](#label)** | | ✅ |  A concise summary of what you associate with a topic. |
| **[Topic Sentiment](#topic-sentiment)** | ✅ | ✅ | If this topic has a *positive, negative and neutral* version.  |
| **[Sentiment Labels](#sentiment-Labels)** | ✅ | ✅ | Optional sentiment-specific topic labels. |
| [Description](#description) |  | | Optional long-form description or examples. |
| [Code](#code) |  |  | Optional unique, numeric identifier for the topic & sentiment.|

<!-- theme: info -->

> ***AI-relevant 🤖** means the property is considered by the AI during training and when assigning topics.

### Category

A category is a set of topics which are referring to the same overarching theme. A category could be for example `Customer Service`.

*The category is AI-relevant 🤖*.

### Label

Concise meaning of the topic. This is what's displayed on the topic chips and is used by our AI to assign topics to texts. A good topic name should be short while still conveying the meaning of the topic in plain text. Examples for topic names are `Staff friendliness` or `Shipping Fees`.

*The label is AI-relevant 🤖*.

### Topic Sentiment

If the AI should distinguish between *positive, negative and neutral* versions of this topic. For most topics you will want this to be enabled, but there are topics like `Not relevant` or `Don't know` where topic sentiment does not make sense.

*The topic sentiment setting is AI-relevant 🤖*.

<!-- theme: warning -->
> #### Disabling & enabling topic sentiment
>
> When disabling the topic sentiment, the sentiment will be discarded from the topic in all rows. **This action is non-reversible:** If you activate the sentiment again, rows which have already been reviewed will not get the topic sentiment back but will show a `neutral` sentiment for this topic instead.
>
>For rows which haven't been reviewed yet, the AI will start differentiating between the sentiment versions as soon as you enable the topic sentiment.

### Sentiment Labels

Optional sentiment-specific topic labels, which are displayed on topic chips and charts instead of the topic label   itself. 
*Example:* `Friendly` / `Unfriendly` for topic name `Friendliness`. <br>Only available if topic-sentiment is enabled.

*The sentiment labels are AI-relevant 🤖*.

### Description

Longer description of the topic for reference. This field is not used by our AI to assign the topic, therefore make sure that the essence of the description is contained in the topic label & category.

### Code

Unique numerical identifier for a specific topic and its sentiment. This can be used to visualize and compare across studies or to trigger predefined actions based on the assigned topic and its sentiment. You can choose the code if you want to, otherwise we automatically assign one.

### Deprecation of Keywords

We have decided to deprecate the current version of keywords. The reason for this is that we saw most people using them in a suboptimal way, resulting in **a lower quality of output and more effort** for them.

**What does deprecation mean:** Keywords are disabled by default when switching to v2, thus being ignored by the AI. If you are sure your usage of them made sense and is important to your projects, please reach out to our support team *indicating an example project where you need them*, and we will see if it makes sense to keep them activated for you.

<!-- theme: success -->

> #### New keyword feature in the pipeline
>
> We are planning to roll out a new version of keywords going forward: Unlike the previous version of keywords which were *interpreted* by the AI, the new keywords will act as *exact matches* and also support *regular expressions*.
> 
> Use-cases for these new keywords could be matching phone numbers or matching different brand names to a company.
>
> Reach out to our support team if you're interested in an early preview.



