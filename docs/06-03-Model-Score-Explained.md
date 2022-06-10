---
stoplight-id: 018wy3xdq3han
---

# AI Quality Score
**The score measures how well your coding matches the automatic one of the model.** It becomes available when you have reviewed > 50 verbatims.The score represents the Weighted F1 of all codes.

## What is a good score?

The theoretical maximum is 100, but this is never reached. A few benchmarks:

- We had the same person (a coding professional) annotate the same text to analyze twice. She achieved an overlap of the two iterations of around **90**.
- When two different people code the same text base, they usually achieve an overlap score in the **70s to 80s**.
- When aiming for "human-level" performance, it makes sense to aim at a score in the **70s**. However, for many applications (such as getting a reliable distribution), a lower score is already sufficient – given there are enough samples.

## Why don't you state the accuracy measure?

For text classification, accuracy is often not a very good measure. If datasets are unbalanced, which is almost always the case when tagging texts (codes usually are not present at a much higher rate than being present), the accuracy would almost always be ridiculously high (above 98%), but not meaningful.

## How do you measure the score?

When training our machine learning models, we leave out a part of the data you have annotated. Scoring is then done on the left out data.

## How do I get to a higher score?

Before focusing purely on the score, be sure to also check a few responses in the middle and towards the end of your dataset for their qualitative performance (remember, we sort the responses by difficulty, with the easiest ones coming last). Sometimes even a low numeric score can still lead to qualitatively good results. To improve the score, there are a few strategies:

- **Streamline your topic collection**: A very large topic collection is more difficult to learn than a slimmer one. As humans would, the model will also make more mistakes distinguishing between similar / not well differentiated topics.
- **Optimize topic names**: The model also takes the topic names into account. Therefore, make sure the topic names are meaningful and not too abstract.
- **Review more examples**: The more examples the model has, the better it will become. If you have "historical" data which is already analyzed but not uploaded to Caplena, contact support to help you ingest that into your account.
- If you're unsure, please contact [support](support@caplena.com) any time, we're happy to have a quick look into your data.