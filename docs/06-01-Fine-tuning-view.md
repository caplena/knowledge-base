---
stoplight-id: b2f8d57b8eb95
---

# Fine-Tuning View

As the name suggests fine-tune the AI towards your specific needs, by reviewing a small portion of your data. The view also allows **modifying topics, filtering and exporting the data**.

* [Fine-Tuning](#fine-tuning)
  * [Reviewing a Row](#reviewing-a-row)
  * [Focus Mode](#focus-mode)
  * [Bulk Assignment](#bulk-assignment)
* [User Interface](#user-interface)
  * [Rows](#rows)
  * [Filters](#filters)
  * [View Options](#view-options)
  * [Export](#export)
  * [Topic Editor](#topic-editor)
  * [AI Score](#ai-score)
  * [Result Chart](#result-chart)
  * [Statistics](#statistics)


## Fine-Tuning

The purpose of fine-tuning is to nudge the AI into the right direction, by providing some additional **training data.** This process is called **reviewing** and achieved by either confirming the AIs topic assignments or changing them to match your expectations for a couple of rows.

<!-- theme: success -->

> The recommended way to go about this is by using the **Focus Mode 🤓**. Alternatively you can also click on a specific row you want to edit, which will open the sidebar.

See [this article](03-02-AI-assignments.md) to learn more about how the AI assigns topics.

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

> The AI automatically updates the topics assignment every now and then in the background after you have made enough reviews or made changes to the topics. See [this article](03-02-AI-assignments.md#when-is-the-ai-updated) to learn when exactly updates are performed.

### Bulk Assignment

In some cases, you might want to perform bulk operations on multiple rows at once. To do this, either select multiple rows by clicking them while holding down the `shift` key. To select all rows that match a certain condition, filter for those rows first and then click the `Select all rows` link on the top right of the row browser.

As soon as multiple rows have been selected, the bulk editing menu opens in the sidebar.


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

See also **TODO: Translations**

#### 2. Assigned Topics

Here you see which topics have been assigned to the row. In this example we have the topics:
* `Rates` with a positive sentiment, belonging to the category `PRICING`
* `Unlimited Date` without sentiment, belonging to the category `PLAN`

Topics are auto-assigned by the AI (see [this article](03-02-AI-assignments.md) on how AI updates work) or can be manually changed by clicking on the row.

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

To edit the topics of multiple rows at once, click this checkbox or hold shift and select multiple rows. See also [here](03-03-Changing-topic-assignments.md#bulk-assignment).

#### 8. Duplicates

If this icon is shown, it means the text of this row is identical to one or more other rows. The number besides the icon indicates how many exact duplicates are present in the project. The duplicates are based on the translated text if translations are enabled.

By default, duplicates are assigned the same topics and are also marked as *reviewed*, when you review one of them. To disable this behavior, adjust the duplicates grouping setting in the [view options](#view-options).

<!-- theme: info -->
> Duplicate grouping may be *temporarily disabled* if specific filters are applied (e.g. when filtering for other columns in your data), to prevent confusing behavior. A notification is shown on the top right whenever this is the case.

#### 9. See Original Text

If translations are enabled, you can toggle between the translated text and the original one with this button. To define which text should be shown for all rows, open the [view options](#view-options).

See also translations. [TODO]

### Filters

Add filters to only show a subset of all rows. Filters are also applied to exports triggered from this view, see [this article](03-04-Export.md).

![Filters](images/filters.png)

### View Options

The view options allow you to specify a couple of settings which define the appearance of your data:
* **Display additional columns:** Which additional data columns from your project to show below the text. See also [Other Columns](#3-other-columns).
* **Group identical responses:** If enabled (default), duplicate texts are only shown once. [Learn more](#8-duplicates).
* **Show Translations:** If enabled, the translations are shown instead of the original text. This is the default if translations were enabled for the project when importing the data. See also [TODO].


### Export

See [Export](03-04-Export.md).


### Topic Editor

In the topic editor you can
* edit topic properties, *by clicking on them*
* merge or combine them to sentiment topics, *by dragging them onto each other*
* add new topics or categories

To learn more about how topics work, see also [Topics.](02-01-Topics.md)

<!-- theme: info -->
> Whenever topics are changed or added, this triggers an AI update. See also [AI Topic Assignments](03-02-AI-assignments.md#when-is-the-ai-updated).

### AI Score

See [AI Score](03-02-AI-assignments.md#ai-score).

### Result Chart

Get a live overview of the current distribution of topics. [TODO Screenshot]

### Statistics

See some stats on your project.
