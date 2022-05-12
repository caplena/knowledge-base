# What's new

* [Sentiment Topics](#sentiment-topics)
* [New Fine-Tuning view](#new-fine-tuning-view)
* [Deduction of credits on Upload](#deduction-of-credits-on-upload)
* [API v2](#api-v2)

## Sentiment Topics 👍

Codes are now called **topics**. And they can now have different sentiments:

| Positive | Neutral  | Negative  |
|---|---|---|
| <img src="https://raw.github.com/caplena/knowledge-base/master/docs/images/topic_positive.png" style="width:170px;"/> | <img src="https://raw.github.com/caplena/knowledge-base/master/docs/images/topic_neutral.png" style="width:170px;"/> |  <img src="https://raw.github.com/caplena/knowledge-base/master/docs/images/topic_negative.png" style="width:170px;"/> |

[👉 Learn more.](02-01-Topics.md) on how topics work.

Check out the [🚀 Migration Guide](01-01-Migration-guide.md) to see how to make use of sentiment topics in existing projects.

## New Fine-Tuning View

We have completely redone the view where you can fine-tune the AI. Besides a better UI we haveimplemented a myriad of new features and improvements, including:
* More powerful filtering
* Improved bulk editing
* Displaying more data, i.e. other columns of your project
* Downloading of filtered data

## Deduction of Credits on Upload

For all new projects or when appending rows to an existing projects, **credits will be billed on upload immediately**.

*Why?* When starting out we wanted to make it as easy as possible to experiment with our app and therefore only billed on download. As the application matured we added more and more features. At the same time your projects grew bigger and bigger (up to 400k rows 🐳). This lead to increased infrastructure costs on our side (translations, review scraping, AI training, etc.), so we had to implement rules to bill on upload in *some* cases (e.g. when translations were activated *and* the project was large *or* the source was reviews).

Over time the rules grew ever more complex and the moment of deduction became unclear, which lead to a lot of confusion on our customers's side. Thus we decided to simplify things: Credits are billed on upload.

<!-- theme: info -->

> #### What about testing & mistakes?
> For this purpose everyone gets a free trial. Furthermore, there are two demo projects in every account, which of course don't incur any costs. For other experiments just upload small datasets.
>
> For honest mistakes on upload, we are accommodating in reimbursing the credits, at least in part (minus potential translation costs which we directly pay to third-parties).

## API v2

[TODO]

