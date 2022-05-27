---
stoplight-id: vdo41jr6e3rau
---

# How Automatic Translations Work

## How to enable automatic translations?
During upload, choose Yes on the Automatic Translation select menu.

![Bildschirmfoto 2022-05-27 um 12.04.50.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/wgjJucn9BUQ)

## Into what language are the answers translated?
They are translated to the main language selected during upload. We strongly recommend to set this to the same language you'll create your topic collection in.

## How is the source language determined?
By default, the source language is detected automatically for every answer. The text will be translated only if it is not already in the main language. If you already know the source language of your responses you can supply this information in the upload by adding a column with [ISO 639-1 language codes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes). We will recognise such columns automatically during upload and utilise the supplied source language instead of the automatic detection.

![Screenshot 2021-06-02 at 10.02.52.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/WurMrFuExtU)

You can also have empty cells in your source language columns, for these rows we will then apply the automatic detection.

