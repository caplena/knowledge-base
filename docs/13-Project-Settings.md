---
stoplight-id: n3cuant6i94ec
---

# Project Settings

Once you've imported and organized your data, click on "Continue to Settings" to configure project settings.

![Screenshot 2024-06-26 at 14.29.46.png](<../assets/images/Screenshot 2024-06-26 at 14.29.46.png>)

Here, you can:

- Assign a name to your project.
- Add tags for easy project sorting in the future.
- Set the language for your topic collection.
Below, you'll find advanced settings:

- Enable translations if you wish to translate your verbatims into another language.
- Enable anonymization to remove personal identifiable information (PII) from all text comments.

## Anonymize Text Comments

Caplena can automatically remove the following personal identifiable information (PII) from all text comments:
* Name
* Address
* Email
* Phone Number
* Bank Account
* Credit Card Number
* Passport Number
* Username
* Password
* Driver License
* Healthcare Number
* other numerical PII like computer MAC addresses

If your plan includes anonymization, you can toggle it with a checkbox in the Project settings during the upload process:

![Screenshot 2024-09-03 at 10.14.48.png](<../assets/images/Screenshot 2024-09-03 at 10.14.48.png>)


Note that the anonymization process *cannot be undone* as only the anonymized data is stored on Caplena.

The PII is replaced by placeholders indicating what kind of PII has been removed:

![Screenshot 2022-06-01 at 15.35.41.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/7MS4c2V5Lqw)

The anonymization process takes place right after the upload onto the Caplena server. The original data - the data that includes the PII information – will not be visible at any time. For technical reasons, the original data that includes the PII information will remain on the Caplena server for a short period of time, before it will be automatically and permanently deleted from the server and its backup system.

### Anonymization and Translations

Anonymization operates on the source text and is performed **before** translation. This means that if the source text was anonymized, the translated text will be anonymized too. However, not all languages are supported for anonymization. Here's a list of supported languages:

| Language               | ISO Code  |
|------------------------|-----------|
| Afrikaans              | af        |
| Arabic                 | ar        |
| Bambara                | bm        |
| Belarusian             | be        |
| Bengali                | bn        |
| Bulgarian              | bg        |
| Burmese                | my        |
| Cantonese (traditional)| zh-TW     |
| Catalan                | ca        |
| Croatian               | hr        |
| Czech                  | cs        |
| Danish                 | da        |
| Dutch                  | nl        |
| English                | en        |
| Estonian               | et        |
| Finnish                | fi        |
| French                 | fr        |
| Georgian               | ka        |
| German                 | de        |
| Greek                  | el        |
| Hebrew                 | he        |
| Hindi                  | hi        |
| Hungarian              | hu        |
| Icelandic              | is        |
| Indonesian             | id        |
| Italian                | it        |
| Japanese               | ja        |
| Khmer                  | km        |
| Korean                 | ko        |
| Latvian                | lv        |
| Lithuanian             | lt        |
| Luxembourgish          | lb        |
| Malay                  | ms        |
| Mandarin (simplified)  | zh-CN     |
| Moldovan               | ro        |
| Norwegian (Bokmål)     | nb        |
| Persian (Farsi)        | fa        |
| Polish                 | pl        |
| Portuguese             | pt        |
| Punjabi                | pa        |
| Romanian               | ro        |
| Russian                | ru        |
| Slovak                 | sk        |
| Slovenian              | sl        |
| Spanish                | es        |
| Swahili                | sw        |
| Swedish                | sv        |
| Tagalog                | tl        |
| Tamil                  | ta        |
| Thai                   | th        |
| Turkish                | tr        |
| Ukrainian              | uk        |
| Vietnamese             | vi        |

Texts in other languages will be not or only partially anonymized. We'll add more languages in upcoming releases.


## Auto-Translation
You can enable [automatic translation](#auto-translation-in-detail) with the click of a button. Through that functionality, the application will work on practically any language.

## Topic Collection Language

Caplena is inherently multilingual and it can work with topic collections in any language and the topics do not necessarily have to be in the same language as the answers.

However, for performance reasons we strongly recommend to create your topics in the same language as most of the answers in your project. If most answers are in English, the topics should be in English too. If your data spans across multiple projects, we also recommend using the same language as most of the answers.

When translations are enabled, we suggest writing the topics in the language the responses were translated to (either English or German etc.). This ensures optimal results and helps us to improve the service.

The language selected as main topic language will also be the language shown as labels when creating charts.

## Auto-Translation in Detail

### Enable Auto-Translation

In the project setting switch on the toggle to enable the translations of your text. You can chose between DeepL and Google Translate.

![Bildschirmfoto 2024-03-11 um 16.41.45.png](<../assets/images/Bildschirmfoto 2024-03-11 um 16.41.45.png>)


### Main Language

Text to analyze will be translated into the main language selected during upload. We strongly recommend to set this to the same language you'll create your topic collection in.

### Language Determination

By default, the source language is detected automatically for every answer. The text will be translated only if it is not already in the main language. If you already know the source language of your responses you can supply this information in the upload by adding a column with [ISO 639-1 language codes](https://en.wikipedia.org/wiki/List_of_ISO\_639-1\_codes). We will recognise such columns automatically during upload and utilise the supplied source language instead of the automatic detection.

![Screenshot 2021-06-02 at 10.02.52.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/WurMrFuExtU)

You can also have empty cells in your source language columns, for these rows we will then apply the automatic detection.

### Does it cost anything?

Fees for automatic translation services are already included in your subscription and your Ad-Hoc credits, no additional charges incur for translations.

### When to use it?

We strongly recommend turning on automatic translations in the following cases:

1. You have a multilingual text to analyze with different languages in the same dataset (e.g. the topic collection will be in English but the texts are in Chinese, English, German, etc.);
2. Your text to analyze is in a language that is not supported by Caplena (see [supported languages](https://caplena.com/en/supported-languages/));
3. You need your topic collection to be in a different language than the text to analyze;
4. You don't speak the language the texts to analyze are in and thus require translations 🙂.

### Google Translate & DeepL

DeepL is a newish player with very good translation quality, however only a limited set of languages is supported (click on "Supported languages" during the upload process to learn more). Anecdotally, we've found DeepL to yield a bit better results.

If you choose DeepL we will use DeepL for supported languages and fallback to Google Translated for the languages that are only supported by Google Translate. For a list of supported languages, see below.


### Source Language

The source language can be determined and specified during data upload, see [here](#language-determination) for information on how to upload with source language and its implications. You can of course also supply the source language when uploading via API by populating the `source_language` attribute of your answers.

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

## Supported Languages



Caplena supports a range of languages out of the box, check out [this list](https://caplena.com/en/supported-languages/) for details.

Caplena works best on languages for which we have a lot of data, specifically Western European languages. This doesn't mean other languages won't work at all, but such datasets might need a bit more manual fine-tuning from your side.

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
