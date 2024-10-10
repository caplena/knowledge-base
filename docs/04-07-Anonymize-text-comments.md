---
stoplight-id: waiokjkj9al83
---

# Anonymize Text Comments

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