---
stoplight-id: b2f8d57b8eb95
---

# Fine-Tuning View

As the name suggests fine-tune the AI towards your specific needs, by reviewing a small portion of your data. The view also allows **modifying topics, filtering and exporting the data**.

* [Fine-Tuning](#fine-tuning)
  * [Reviewing a Row](#reviewing-a-row)
  * [Focus Mode](#focus-mode)
  * [Bulk Assignment](#bulk-assignment)
  * [When is the AI updated?](#when-is-the-ai-updated)
  * [When is the AI fine-tuned enough?](#when-is-the-ai-fine-tuned-enough)
  * [AI Score](#ai-score)
* [User Interface](#user-interface)
  * [Rows](#rows)
  * [Filters](#filters)
  * [View Options](#view-options)
  * [Export](#export)
  * [Topic Editor](#topic-editor)
  * [AI Score](#ai-score)
  * [Result Chart](#result-chart)
  * [Statistics & Number of Rows](#statistics-number-of-rows)


## Fine-Tuning

The purpose of fine-tuning is to nudge the AI into the right direction, by providing some additional **training data.** This process is called **reviewing** and achieved by either confirming the AIs topic assignments or changing them to match your expectations for a couple of rows.

https://youtu.be/OyQjsKhHZAs

<!-- theme: success -->

> The recommended way to go about this is by using the **Focus Mode 🤓**. Alternatively you can also click on a specific row you want to edit, which will open the sidebar.

See [this article](06-02-AI-assignments.md) to learn more about how the AI assigns topics.

### Focus Mode

Activate the focus mode by clicking the icon on the top right of the fine-tuning view.

![Assigning Topics](images/focus-view-button.png)

This mode does a couple of things:
* The rows are **sorted** by **AI certainty**: This means that you will first be shown the texts where the AI is *most unsure* on its assignments. By reviewing and potentially correcting these assignments first, the AI learns much more efficiently.<br>This technique is also known as *active learning*.
* Only non-reviewed rows will be shown, as you do not want to look at already reviewed rows again.
* Any potential distractions are hidden, so you can fully focus on the content of the text.

### Reviewing a Row

![Assigning Topics](images/assign-topics-sidebar.png)

In the focus mode or the sidebar you can perform these actions:
* **Adding topics** from the topic select list. For sentiment topics a specific sentiment must be chosen.
* **Removing topics** from the already applied topics by clicking their remove icon.
* **Rearranging topics** by dragging them into the desired order.
* **Changing the topic sentiment** of already applied topics by clicking their sentiment indicator.

A row is automatically marked as *reviewed* when you change anything on the topics. 
To mark a row as reviewed without making a change, either press `cmd + enter` (Mac) / `ctrl + enter` (Windows) or click the *Mark as reviewed & next* button.

![Marking as reviewed](images/mark-as-reviewed.png)

<!-- theme: info -->

> The AI automatically updates the topics assignment every now and then in the background after you have made enough reviews or made changes to the topics. See [this article](#when-is-the-ai-updated) to learn when exactly updates are performed.

### Bulk Assignment

In some cases, you might want to perform bulk operations on multiple rows at once. To do this, either select multiple rows by clicking them while holding down the `shift` key. To select all rows that match a certain condition, filter for those rows first and then click the `Select all rows` link on the top right of the row browser.

As soon as multiple rows have been selected, the bulk editing menu opens in the sidebar.

### When is the AI updated?

#### 1. After enough Reviews

As you review rows, a counter will indicate when the next AI update will be triggered. The first update happens after 20 reviews, the second after 50, then 100 and so on.

The "distance" between updates gets larger as trainings become more computationally expensive and the incremental amount of information gained from a review decreases with the amount of data.

*Note:* [Bulk assignments](03-03-Changing-topic-assignments.md#bulk-assignment) only count as a single review.

![AI Update](images/ai-next-update.png)


#### 2. When changing Topics

If any of the [AI-relevant topic properties](03-01-Topics.md#topic-properties) are changed, the AI will be fine-tuned again. In some cases, a delay of 30-60 seconds is applied before starting the update.

### When is the AI fine-tuned enough?

You can decide when you are satisfied with fine-tuning. We recommend using a combination of a qualitative check and consulting the AI score to make this decision.

<!-- theme: info -->
> As a rule of thumb, we often recommend to review about 20% of the rows but not more than 300, whichever is lower.

### AI Score

The AI score indicates how well **your reviewed topic assignments match the AI's auto-assignments.**

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

Under the hood, the model does not only forcast coding for the rows, but also a certainty measure for those predictions. We can estimate the AI score starting from such certaintly measures.

Technically speaking the score represents the weighted F1 over all topics.


#### How do I get to a higher score?

Before focusing purely on the score, be sure to also check the topic assignments for a few rows qualitatively. Sometimes even a low numeric score can still lead to qualitatively good results. To improve the score, there are a few strategies:

* **Streamline your topic collection:** A very large number of topics is more difficult to assign than when having fewer. As humans would, the AI will also make more mistakes distinguishing between similar / not well differentiated topics.
* **Optimize topic labels:** The AI takes the topic & category labels into account. Therefore, make sure the topic labels are meaningful and not too abstract.
* **Review more rows:** The more examples the AI has to learn from, the better it will become. If you have "historical" data which already has topics assigned but is not uploaded to Caplena yet, contact [support](support@caplena.com) to help you ingest that into your account.

For enterprise customers we are also happy to have one of our language specialists look into your data, just contact [support](support@caplena.com).


## User Interface

![Data view](images/fine-tuning-view.png)
1. [Rows](#rows)
2. [Filters](#filters)
3. [View Options](#view-options)
4. [Export](#export)
5. [Topic Editor](#topic-editor)
6. [AI Score](#ai-score)
7. [Result Chart](#result-chart)
8. [Statistics](#statistics)

### Rows

Here the text to analyze is displayed, alongside the assigned topics.

![Row](images/fine-tuning-row.png)

#### 1. Text

If translations have been activated for this project and set to be shown in the [view options](#view-options) (enabled by default, if project is translated), the translated text is shown here. To toggle to the source language version, click the *See original* button (element 9 in screenshot above).

See [here](09-01-Languages.md) for more information on how translations work.

#### 2. Assigned Topics

Here you see which topics have been assigned to the row. In this example we have the topics:
* `Rates` with a positive sentiment, belonging to the category `PRICING`
* `Unlimited Date` without sentiment, belonging to the category `PLAN`

Topics are auto-assigned by the AI (see [this article](06-02-AI-assignments.md) on how AI updates work) or can be manually changed by clicking on the row.

#### 3. Other Columns

Other columns of your project can be displayed alongside the text. Click the cogwheel icon or open the [view options](#view-options) to choose which columns to display.

#### 4. Overall Sentiment

The overall sentiment of the text can be either *positive, neutral or negative*.

![Row](images/sentiments.png)

It is computed automatically and cannot be adjusted manually. However, when sentiment-enabled topics are assigned to the text, the overall sentiment is adapted accordingly.

Given at least one sentiment-enabled topic is present, the formula for the sentiment is:

```
sentiment_sum = sum_over_topics(1 if topic is positive | 0 if topic is neutral | -1 if topic is negative)
sentiment_average = sentiment_sum / number_of_topics
if (sentiment_average > 0.33) return 'positive'
if (sentiment_average < -0.33) return 'negative'
else return 'neutral'
```

#### 5. Reviewed State

The checkbox indicates this row has been set as reviewed. Reviewed rows are not modified by the AI anymore but are used as training data for the AI when fine-tuning. When analyzing, visualizing or exporting the data, it is not relevant if a row has been reviewed or not.

#### 6. Row Number

This is the index of the row in the project you uploaded / imported into Caplena.

#### 7. Bulk Select Checkbox

To edit the topics of multiple rows at once, click this checkbox or hold shift and select multiple rows. See also [here](#bulk-assignment).

#### 8. Duplicates

If this icon is shown, it means the text of this row is identical to one or more other rows. The number besides the icon indicates how many exact duplicates are present in the project. The duplicates are based on the translated text if translations are enabled.

By default, duplicates are assigned the same topics and are also marked as *reviewed*, when you review one of them. To disable this behavior, adjust the duplicates grouping setting in the [view options](#view-options).

<!-- theme: info -->
> Duplicate grouping may be *temporarily disabled* if specific filters are applied (e.g. when filtering for other columns in your data), to prevent confusing behavior. A notification is shown on the top right whenever this is the case.

#### 9. See Original Text

If translations are enabled, you can toggle between the translated text and the original one with this button. To define which text should be shown for all rows, open the [view options](#view-options).

See [here](09-01-Languages.md) for more information on how translations work.

### Filters

Add filters to only show a subset of all rows. Filters are also applied to exports triggered from this view, see [this article](04-07-Export.md).

![Filters](images/filters.png)

### View Options

The view options allow you to specify a couple of settings which define the appearance of your data:
* **Display additional columns:** Which additional data columns from your project to show below the text. See also [Other Columns](#3-other-columns).
* **Group identical responses:** If enabled (default), duplicate texts are only shown once. [Learn more](#8-duplicates).
* **Show Translations:** If enabled, the translations are shown instead of the original text. This is the default if translations were enabled for the project when importing the data. See also [here](09-01-Languages.md).


### Export

See [Export](04-08-Export.md).


### Topic Editor

In the topic editor you can
* edit topic properties, *by clicking on them*
* merge or combine them to sentiment topics, *by dragging them onto each other*
* add new topics or categories

https://youtu.be/j3quiv6lTqE

To learn more about how topics work, see also [Topics.](03-01-Topics.md)

<!-- theme: info -->
> Whenever topics are changed or added, this triggers an AI update. See also [AI Topic Assignments](#when-is-the-ai-updated).

### AI Score

See [AI Score](#ai-score).

### Result Chart

Get a live overview of the current distribution of topics.

![Bildschirmfoto 2022-08-25 um 19.26.16.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/VWz14Em7Wpk)


### Statistics & Number of Rows

See some core statistics of this column / project.

<!-- theme: info -->
> A common question is why the number of rows stated in the statistics **doesn't match the number** shown in the bottom left of the row browser or the top right *Select all rows* link.
> 
> The reason for these potential discrepancies are [duplicates](#8-duplicates), which are *hidden* by default in the row browser (thus resulting in a lower number of rows) but *are* counted in the `Statistics` section. Grouping of duplicates can be disabled in the [view options](#view-options).
