---
stoplight-id: 8l4bcrf260ng2
---

# Languages and Translations

## Auto-Translation
You can enable [automatic translation](#auto-translation-in-detail) with the click of a button. Through that functionality, the application will work on practically any language. In the project setting switch on the toggle to enable the translations of your text. You can chose between DeepL and Google Translate.

![Bildschirmfoto 2024-03-11 um 16.41.45.png](<../assets/images/Bildschirmfoto 2024-03-11 um 16.41.45.png>)

Text to analyze will be translated into the main language selected during upload. We strongly recommend to set this to the same language you'll create your topic collection in.

### When to use it?

We strongly recommend turning on automatic translations in the following cases:

1. You have a multilingual text to analyze with different languages in the same dataset (e.g. the topic collection will be in English but the texts are in Chinese, English, German, etc.);
2. Your text to analyze is in a language that is not supported by Caplena (see [supported languages](https://caplena.com/en/supported-languages/));
3. You need your topic collection to be in a different language than the text to analyze;
4. You don't speak the language the texts to analyze are in and thus require translations 🙂.

## Supported Languages

Caplena supports a range of languages out of the box, check out [this list](https://caplena.com/en/supported-languages/) for details.

Caplena works best on languages for which we have a lot of data, specifically Western European languages. This doesn't mean other languages won't work at all, but such datasets might need a bit more manual fine-tuning from your side.



### Does it cost anything?

Fees for automatic translation services are already included in your subscription and your Ad-Hoc credits, no additional charges incur for translations.


### Google Translate & DeepL

DeepL is a newish player with very good translation quality, however only a limited set of languages is supported (click on "Supported languages" during the upload process to learn more). Anecdotally, we've found DeepL to yield a bit better results.

If you choose DeepL we will use DeepL for supported languages and fallback to Google Translated for the languages that are only supported by Google Translate. For a list of supported languages, see below.

Language | Google-Translate | DeepL
---------|----------|---------
 Bulgarian  | ✓ | ✓
 Chinese (Simplified)  | ✓ | ✓
 Chinese (Traditional)  | ✓ | 
 Czech  | ✓ | ✓
 Danish  | ✓ | ✓
 Dutch  | ✓ | ✓
 English | ✓ | ✓
 Estonian  | ✓ | ✓
 Finnish  | ✓ | ✓
 French  | ✓ | ✓
 German  | ✓ | ✓
 Greek  | ✓ | ✓
 Hungarian  | ✓ | ✓
 Indionesean  | ✓ | ✓
 Italian  | ✓ | ✓
 Japanese  | ✓ | ✓
 Latvian  | ✓ | ✓
 Lithuanian  | ✓ | ✓
 Polish  | ✓ | ✓
 Portuguese  | ✓ | ✓
 Romanian  | ✓ | ✓
 Russian  | ✓ | ✓
 Slovak  | ✓ | ✓
 Slovenian  | ✓ | ✓
 Spanish  | ✓ | ✓
 Swedish  | ✓ | ✓
 Turksih  | ✓ | ✓
 Afrikaans  | ✓ | 
 Albanian  | ✓ | 
 Arabic  | ✓ | 
 Malay  | ✓ | 
 Punjabi  | ✓ | 
 Thai  | ✓ | 
 Vietnamese  | ✓ |
 ...more  |[Google Language Support](https://cloud.google.com/translate/docs/languages) | 


### Language Determination

By default, the source language is detected automatically for every answer. The text will be translated only if it is not already in the main language. If you already know the source language of your responses you can supply this information in the upload by adding a column with [ISO 639-1 language codes](https://en.wikipedia.org/wiki/List_of_ISO\_639-1\_codes). We will recognise such columns automatically during upload and utilise the supplied source language instead of the automatic detection.

![Screenshot 2021-06-02 at 10.02.52.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/WurMrFuExtU)

You can also have empty cells in your source language columns, for these rows we will then apply the automatic detection.


### Visibility of Translations

You can view and export both translated and the original texts in our app. Available options depend on where you are in the application.

#### Fine-Tuning View

Both translated and original text is visible. Switch between displaying source or translated text using the *See original* / *See translated* function on the bottom right of each text to analzye. Translated text is shown as default.

![Bildschirmfoto 2022-06-02 um 10.19.15.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/OpwsyWRyg1w)

![Bildschirmfoto 2022-06-02 um 10.20.34.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/xrAX6JO6pPk)


#### Visualizations

All charts are interactive. By clicking on a chart element such as a bar or tile the verbatim browser will open, allowing you to see all texts behind the selected topic. Translations can be enabled / disabled at the top of the row browser window. The source language can be seen when hovering over the translation icon on front of the text.

![Bildschirmfoto 2022-06-02 um 11.05.38.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/SBF5iOsdxVA)

#### Data Export

When exporting the data, translations will be included by default. Using the "Advanced options" you can change the column position of the translated text or exclude it from the export file.

![Bildschirmfoto 2022-06-02 um 11.16.48.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/fpyzxNInwko)


