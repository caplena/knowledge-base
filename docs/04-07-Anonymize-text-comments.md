---
stoplight-id: hzrjzb1fw3n55
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

If your plan includes anonymization, you can toggle it on in the Project settings during the upload process:

![Screenshot 2024-05-09 at 15.45.17.png](<../assets/images/Screenshot 2024-05-09 at 15.45.17.png>)


Note that the anonymization process *cannot be undone* as only the anonymized data is stored on Caplena.

The PII is replaced by placeholders indicating what kind of PII has been removed:

![Screenshot 2022-06-01 at 15.35.41.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/7MS4c2V5Lqw)

The anonymization process takes place right after the upload onto the Caplena server. The original data - the data that includes the PII information – will not be visible at any time. For technical reasons, the original data that includes the PII information will remain on the Caplena server for a short period of time, before it will be automatically and permanently deleted from the server and its backup system.

## Languages and Translations

Anonymization operates on the source text and is performed **before** translation. This means that if the source text was anonymized, the translated text will be anonymized too. However, not all languages are supported for anonymization. Here's a list of supported languages:
* Arabic
* Belarusian
* Bengali
* Bulgarian
* Burmese
* Catalan
* Croatian
* Czech
* Danish
* Dutch
* English
* Estonian
* Finnish
* French
* German
* Greek
* Hebrew
* Hindi
* Hungarian
* Icelandic
* Indonesian
* Italian
* Japanese
* Khmer
* Korean
* Latvian
* Lithuanian
* Luxembourgish
* Malay
* Mandarin (simplified)
* Moldovian
* Norwegian (Bokmål)
* Persian (Farsi)
* Polish
* Portuguese
* Romanian
* Russian
* Slovak
* Slovenian
* Spanish
* Swahili
* Swedish
* Tagalog
* Thai
* Turkish
* Ukrainian
* Vietnamese

Texts in other languages will be not or only partially anonymized. We'll add more languages in upcoming releases.