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

By default, the source language is detected automatically for every answer. The text will be translated only if it is not already in the main language. If you already know the source language of your responses you can supply this information in the upload by adding a column with [ISO 639-1 language codes](https://en.wikipedia.org/wiki/List_of_ISO\_639-1\_codes). We will recognise such columns automatically during upload and utilise the supplied source language instead of the automatic detection.

![Screenshot 2021-06-02 at 10.02.52.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/WurMrFuExtU)

You can also have empty cells in your source language columns, for these rows we will then apply the automatic detection.

## How much does automatic translation cost?

Fees for automatic translation services are already included in your subscription and your Ad-Hoc credits, no additional charges incur for translations.

## When should I enable the automatic translations?

We strongly recommend turning on automatic translations in the following cases:

1. You have a multilingual text to analyze with different languages in the same dataset (e.g. the topic collection will be in English but the texts are in Chinese, English, German, etc.);
2. Your text to analyze is in a language that is not supported by Caplena (see [supported languages](https://caplena.com/en/supported-languages/));
3. You need your topic collection to be in a different language than the text to analyze;
4. You don't speak the language the texts to analyze are in and thus require translations 🙂.

## How do I chose between Google Translate and DeepL?

DeepL is a newish player with very good translation quality, however only a limited set of languages is supported (click on "Supported languages" during the upload process to learn more). Anecdotally, we've found DeepL to yield a bit better results both with automatic and manual coding. If you choose DeepL and have texts in non-supported languages, you'll get nonsensical answers since DeepL will try to detect the language but fails to do so. It then takes the "closest" language - which will be completely off. We thus recommend Google Translate for studies with non-supported languages.

If you choose DeepL and you supply the source language during upload with languages that are not supported by DeepL, we will use DeepL for supported languages (and for empty source language) and fallback to Google Translated for the languages that are only supported by Google Translate. For a list of supported languages, see below.

## I know how the source language for each of my answers, how can I specify that?

Specifying the source language for answers is possible during upload, see [here](05-03-Automatic-Translation.md#How-is-the-source-language-determined?) for information on how to upload with source language and its implications. You can of course also supply the source language when uploading via API by populating the `source_language` attribute of your answers.

## Where can I see the translated texts?

We allow to view and export both translated and the original texts in our app. Available options depend on the view:

### Fine-Tuning View

Both translated and original text is visible. Switch between displaying source or translated text using the "See original" / "See translated" function on the bottom right of each text to analzye. Translated text is shown as default.

![Bildschirmfoto 2022-06-02 um 10.19.15.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/OpwsyWRyg1w)

![Bildschirmfoto 2022-06-02 um 10.20.34.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/xrAX6JO6pPk)


### Visualizations

All charts are interactive. By clicking on a chart element such as a bar or tile the verbatim browser will open, allowing you to see all texts behind the selected topic. Translations can be enabled / disabled at the top of the text browser window. The source language can be seen when hovering over the translation icon on front of the text.

![Bildschirmfoto 2022-06-02 um 11.05.38.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/SBF5iOsdxVA)

### Data Export

When exporting the data, translations will be included by default. Using the "Advanced options" you can change the column position of the translated text or exclude it from the export file.

![Bildschirmfoto 2022-06-02 um 11.16.48.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/fpyzxNInwko)

## Language-support

Language | Google-Translate | DeepL
---------|----------|---------
 English | ✓ | ✓
 German  | ✓ | ✓
 French  | ✓ | ✓
 Spanish  | ✓ | ✓
 Portuguese  | ✓ | ✓
 Italian  | ✓ | ✓
 Dutch  | ✓ | ✓
 Polish  | ✓ | ✓
 Russian  | ✓ | ✓
 Japanese  | ✓ | ✓
 Chinese (Simplified)  | ✓ | ✓
 Chinese (Traditional)  | ✓ | 
 Bulgarian  | ✓ | ✓
 Czech  | ✓ | ✓
 Danish  | ✓ | ✓
 Greek  | ✓ | ✓
 Estonian  | ✓ | ✓
 Finnish  | ✓ | ✓
 Hungarian  | ✓ | ✓
 Lithuanian  | ✓ | ✓
 Latvian  | ✓ | ✓
 Romanian  | ✓ | ✓
 Slovak  | ✓ | ✓
 Slovenian  | ✓ | ✓
 Swedish  | ✓ | ✓
 Punjabi  | ✓ | 
 Vietnamese  | ✓ | 
 Albanian  | ✓ | 
 Thai  | ✓ | 
 Malay  | ✓ | 
 Arabic  | ✓ | 
 Afrikaans  | ✓ | 
 ...more  |[Google Language Support](https://cloud.google.com/translate/docs/languages) | 


