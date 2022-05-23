---
stoplight-id: ezyy60tig7uzy
---

# Data-Structure - Projects, Text to Analyze, Rows, etc.

## What is a project?

A Project is the highest-level object at Caplena. It is somewhat equivalent to a Sheet in Excel.

![file-dxIlK1wDyy.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/NJX61i3WtD8)

#### Survey Example:
When conducting a survey, you will probably have all results in one sheet. Every row then represents one respondent, every column to either a question or some additional data, like identifier, demographics etc.

#### NPS Feedback Example:
[NPS questionnaires](https://blog.caplena.com/2019/07/22/5-keys-to-effectively-measuring-and-utilizing-nps/) will obviously have a column containing the score (an auxiliary column in Caplena's terms) and often one column containing the open-ended feedback. There might also be multiple questions, e.g. "What did you like..." and "What did you dislike", although we recommend asking only a single question in most cases.

#### Social Media Data Example:
A social media dataset will usually have one column containing the text you want to evaluate, so you would have one question in Caplena's terms. But there will probably be further columns with addition information like user, timestamps or likes.

## What is Text to Analyze (Column)?
Text to analyze is text data in a column of your data file that you wish to analyze with Caplena. So in our example data, we would have two text to analyze columns, with three text comments each. The other two columns are not text to analyze columns, but can be displayed when fine-tuning or used as filters or segments when creating charts and dashboards.

![file-XIQK4zVen1.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/dniurPW2JAA)

## What is a Text Comment?
A text comment is an indiviudal data cell with text to analyze. This could be the open-ended answer from a survey respondent to an open-ended question, the product review from a customer from a review website, or in social media terms: One tweet or one post.

![file-IUbEWmXUkY.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/xNLMfbsk8qY)

## What is a row?

A row is the same as what it is in Excel: A row of data 😊. When appending additional data to your projects, you can only do this row-wise (i.e. you cannot upload a response to only one question - all questions in a project always need to have the same number of answers).

