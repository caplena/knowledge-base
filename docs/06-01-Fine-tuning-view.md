---
stoplight-id: b2f8d57b8eb95
---


# Fine-Tuning 

* [Reviewing a Row](#reviewing-a-row)
* [Focus Mode](#focus-mode)
* [Topic Editor](#topic-editor)
* [When should I stop fine-tuning my model?](#when-should-i-stop-fine-tuning-my-model)




The Topic Assignment view is designed to adjust the AI to better meet your specific needs.

![Screenshot 2024-09-06 at 13.56.48.png](<../assets/images/Screenshot 2024-09-06 at 13.56.48.png>)

 By reviewing a small portion of your data, you can refine how the AI interprets and categorizes information. This view also allows you to:

- Modify topics as needed
- Apply filters to focus on specific data segments
- Export the data for further analysis or reporting

Below, you’ll find some information on how to perform reviews.

### Reviewing a Row 
The purpose of fine-tuning is to guide the AI in the right direction by providing it with additional training data. This is done through a process called **reviewing**, where you either confirm the AI's topic assignments or adjust them to better align with your expectations for a few rows. Below, you'll find a video that demonstrates how the process works.

https://youtu.be/OyQjsKhHZAs

<!-- theme: success -->

> The recommended way to go about this is by using the **Focus Mode 🤓**. Alternatively you can also click on a specific row you want to edit, which will open the sidebar.

### Focus Mode

Activate the focus mode by clicking the icon on the top right of the fine-tuning view.

![Assigning Topics](images/focus-view-button.png)

This mode does a couple of things:
* The rows are **sorted** by **AI certainty**: This means that you will first be shown the texts where the AI is *most unsure* on its assignments. By reviewing and potentially correcting these assignments first, the AI learns much more efficiently.<br>This technique is also known as *active learning*.
* Only non-reviewed rows will be shown, as you do not want to look at already reviewed rows again.
* Any potential distractions are hidden, so you can fully focus on the content of the text.



<!-- theme: info -->

> The AI automatically updates the topics assignment every now and then in the background after you have made enough reviews or made changes to the topics. See [this article](#when-is-the-ai-updated) to learn when exactly updates are performed.

### Topic Editor

As the part of the fine-tuning process, you can also:
* edit topic properties, *by clicking on them*
* merge or combine them to sentiment topics, *by dragging them onto each other*
* add new topics or categories

https://youtu.be/j3quiv6lTqE

To learn more about how topics work, see also [Topics.](03-01-Topics.md)

<!-- theme: info -->
> Whenever topics are changed or added, this triggers an AI update. See also [AI Topic Assignments](#when-is-the-ai-updated).

### When should I stop fine-tuning my model?

You can stop fine-tuning whenever you’re satisfied with the results. We recommend using a combination of a **qualitative review** (looking at a sample of rows manually) and checking the **AI score** to make this decision.

<!-- theme: info -->
> Tip: Review about 20% of rows, but not more than 300.

### AI Score

The AI score measures how confident the AI is in assigning topics to your data.

![Screenshot 2024-09-10 at 18.13.07.png](<../assets/images/Screenshot 2024-09-10 at 18.13.07.png>)


#### What is considered a good AI score?

The theoretical maximum score is 100, but this is never reached. A few benchmarks:

- The theoretical maximum score is 100, but this is never reached.
- A single person reassigning topics twice typically achieves a score of 90.
- Two different people assigning topics get scores in the 70s to 80s.
- Aim for 70s for human-level performance. Even lower scores can be sufficient if there’s enough data.


#### How to improve the AI score:

Before focusing purely on the score, be sure to also check the topic assignments for a few rows qualitatively. Sometimes even a low numeric score can still lead to qualitatively good results. To improve the score, there are a few strategies:

* **Streamline your topic collection:** A very large number of topics is more difficult to assign than when having fewer. As humans would, the AI will also make more mistakes distinguishing between similar / not well differentiated topics.
* **Optimize topic labels:** The AI takes the topic & category labels into account. Therefore, make sure the topic labels are meaningful and not too abstract.
* **Review more rows:** The more examples the AI has to learn from, the better it will become. If you have "historical" data which already has topics assigned but is not uploaded to Caplena yet, contact [support](support@caplena.com) to help you ingest that into your account.
* **Review Low AI Score Topics:** On the chart (below the red line) and in the table, you’ll find topics that might be confusing for the AI to classify correctly. These are the topics where the AI has lower confidence in its assignments.

![Screenshot 2024-09-11 at 09.32.34.png](<../assets/images/Screenshot 2024-09-11 at 09.32.34.png>)

The table displays individual AI scores for each topic, allowing you to see how well the AI is performing. Topics with lower scores indicate that the AI had more difficulty assigning them accurately. It’s often a good idea to review responses for the topics with the lowest AI scores. By doing so, you can manually check if the AI’s assignments make sense and correct them if necessary. This can help improve the overall accuracy of the project.

#### Why is there no score for some topics?

If a topic is assigned to very few rows, the AI may not be able to calculate a score. It’s also possible that the AI didn’t understand the topic, though this is rare.


## Topic Assignment User Interface

Please watch this quick walkthrough of the Topic Assignment View: https://www.loom.com/share/c5d42ccac2884111803d7c4946af4465?sid=a0720402-78ed-48e7-bc58-2e248a92e608

You can also find the information about the Topic Assignment View below:


### Rows

#### 1. Text

If translations have been activated for this project and set to be shown in the [view options](#view-options) (enabled by default, if project is translated), the translated text is shown here. To toggle to the source language version, click the *See original* button: 

![Screenshot 2024-09-06 at 17.48.25.png](<../assets/images/Screenshot 2024-09-06 at 17.48.25.png>)


See [here](09-01-Languages.md) for more information on how translations work.

#### 2. Assigned Topics

Here you see which topics have been assigned to the row.

![Screenshot 2024-09-06 at 21.19.37.png](<../assets/images/Screenshot 2024-09-06 at 21.19.37.png>)

 In this example we have the topics:
* `Price` with positive sentiment, belonging to the category `PRICE`
* `Overall quality` with positive sentiment, belonging to the category `QUALITY`

Topics are auto-assigned by the AI (see [this article](06-02-AI-assignments.md) on how AI updates work) or can be manually changed by clicking on the row.

#### 3. Other Columns

Other columns of your project can be displayed alongside the text. Click the cogwheel icon to choose which columns to display.

![Screenshot 2024-09-06 at 21.24.39.png](<../assets/images/Screenshot 2024-09-06 at 21.24.39.png>)



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

![Screenshot 2024-09-06 at 21.31.59.png](<../assets/images/Screenshot 2024-09-06 at 21.31.59.png>)



#### 6. Row Number

This is the index of the row in the project you uploaded / imported into Caplena.

![Screenshot 2024-09-06 at 21.34.35.png](<../assets/images/Screenshot 2024-09-06 at 21.34.35.png>)


#### 7. Bulk Select Checkbox

To edit the topics of multiple rows at once, click this checkbox or hold shift and select multiple rows. See also [here](#bulk-assignment). To select all rows that match a certain condition, filter for those rows first and then click the Select all rows link on the top right of the row browser.

![Screenshot 2024-09-10 at 14.47.22.png](<../assets/images/Screenshot 2024-09-10 at 14.47.22.png>)



#### 8. Duplicates

If this icon is shown, it means the text of this row is identical to one or more other rows. The number besides the icon indicates how many exact duplicates are present in the project. The duplicates are based on the translated text if translations are enabled.

![Screenshot 2024-09-06 at 21.46.54.png](<../assets/images/Screenshot 2024-09-06 at 21.46.54.png>)

By default, duplicates are assigned the same topics and are also marked as *reviewed*, when you review one of them. To disable this behavior, adjust the duplicates grouping setting in the [view options](#view-options).

<!-- theme: info -->
> Duplicate grouping may be *temporarily disabled* if specific filters are applied (e.g. when filtering for other columns in your data), to prevent confusing behavior. A notification is shown on the top right whenever this is the case.

<!-- theme: info -->
> To ensure identical rows are grouped together in your analysis, make sure that all rows have the same status (e.g., all rows should be either reviewed or unreviewed) and have the same topic assigned. 


### Filters

Add filters to only show a subset of all rows. Filters are also applied to exports triggered from this view, see [this article](04-07-Export.md).

![Filters](images/filters.png)

### View Options

The view options allow you to specify a couple of settings which define the appearance of your data:
* **Display additional columns:** Which additional data columns from your project to show below the text. 
* **Group identical responses:** If enabled (default), duplicate texts are only shown once. [
* **Show Translations:** If enabled, the translations are shown instead of the original text. This is the default if translations were enabled for the project when importing the data. See also [here](13-LProject-Settings.md).

![Screenshot 2024-09-10 at 14.50.16.png](<../assets/images/Screenshot 2024-09-10 at 14.50.16.png>)


### Export

With the export options, you can download your results in different formats.

For more information, please see [Export](04-08-Export.md).


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











