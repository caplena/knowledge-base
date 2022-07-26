# Caplena v2

* [What changed](#what-changed)
  * [Sentiment Topics](#sentiment-topics-)
  * [New Fine-Tuning view](#new-fine-tuning-view)
  * [Deduction of credits on Upload](#deduction-of-credits-on-upload)
  * [API v2](#api-v2)
* [Migration Guide](#migration-guide)

## What changed

### Sentiment Topics 👍

Codes are now called **topics**. And they can now have different sentiments:

| Positive | Neutral  | Negative  |
|---|---|---|
| <img src="https://raw.github.com/caplena/knowledge-base/master/docs/images/topic_positive.png" style="width:170px;"/> | <img src="https://raw.github.com/caplena/knowledge-base/master/docs/images/topic_neutral.png" style="width:170px;"/> |  <img src="https://raw.github.com/caplena/knowledge-base/master/docs/images/topic_negative.png" style="width:170px;"/> |

[👉 Learn more.](03-01-Topics.md) on how topics work.

Check out the [🚀 Migration Guide](#migration-guide) to see how to make use of sentiment topics in existing projects.

### New Fine-Tuning View

We have completely redone the view where you can fine-tune the AI. Besides a better UI we have implemented a myriad of new features and improvements, including:
* More powerful filtering
* Improved bulk editing
* Displaying more data, i.e. other columns of your project
* Downloading of filtered data

### Deduction of Credits on Upload

For all new projects or when appending rows to existing projects, **credits will be billed on upload immediately**.

*Why?* When starting out we wanted to make it as easy as possible to experiment with our app and therefore only billed on download. As the application matured, we added more and more features. At the same time your projects grew bigger and bigger (up to 400k rows 🐳). This lead to increased infrastructure costs on our side (translations, review scraping, AI training, etc.), so we had to implement rules to bill on upload in *some* cases (e.g. when translations were activated *and* the project was large *or* the source was reviews).

Over time the rules grew ever more complex, and the moment of deduction became unclear, which lead to a lot of confusion on our customers' side. Thus, we decided to simplify things: Credits are billed on upload.

<!-- theme: info -->

> #### What about testing & mistakes?
> For this purpose, everyone gets a free trial. Furthermore, there are two demo projects in every account, which of course don't incur any costs. For other experiments just upload small datasets.
>
> For honest mistakes on upload, we are accommodating in reimbursing the credits, at least in part (minus potential translation costs which we directly pay to third parties).

### API v2

Our new Caplena v2 API supports topic sentiment plus a myriad of improvements including:
* Extensive filtering capabilities on results and user-provided additional variables
* Ability to fully define the schema of the data along with user-provided references for easier identification
* Simplified output format directly returning topics and sentiment
* Editing and deleting of rows and projects
* Ability to handle large projects > 200k rows

## Migration Guide

**First of all**: *You are not required to convert your projects to use sentiment topics. All previous functionality is still available.*


### Converting Topics to Sentiment Topics

To make use of the new functionality, convert your non-sentiment topics to sentiment topics:

![Merge](images/merge.gif)

1. Drag two corresponding non-sentiment topics, e.g. `Friendly` and `Unfriendly` onto each other. It doesn't matter which one you drag onto the other. A modal will then appear.
2. Activate *"Topic Sentiment"*
3. Adjust the *Topic Label* to be a **Neutral** version of the topic. In our example, this would be `Friendliness`
4. Choose which of the topics represented the *positive* and which represented the `negative` version.
5. Make sure the *sentiment labels* are correct. The *neutral* label can either be left empty (if it is the same as the topic label, it does not make sense to populate it).
6. Hit merge

In case there are rows marked as "reviewed" with the topic you are planning to merge, the review status needs to be changed first to allow enabaling topic level sentiment. Use the filter to select the topics and click on "Select all (number of rows with the topic)". The "Bulk assign" window will open on the right. Under "Row review status" you enable the toggle to "Unreviewed" and you can start the process decribed above.

<!-- theme: info -->
> The codes (numerical IDs) are copied from your previous topics and will thus stay consistent.

<!-- theme: warning -->
> #### Inheriting projects
>
> If you have multiple projects inheriting from each other and still show the old projects in your trend charts, please wait with migrating to the new structure for now.