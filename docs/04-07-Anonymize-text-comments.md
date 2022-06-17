---
stoplight-id: hzrjzb1fw3n55
---

# Anonymize-text-comments

Caplena can automatically remove the following personal identifiable information (PII) from all text comments:
<br><ul class='mt-1 mb-1'><li>Name</li><li>Address</li><li>Email</li><li>Phone Number</li><li>Bank Account</li><li>Credit Card</li><li>Passport Number</li><li>Username</li><li>Password</li><li>Other numerical PII like Healthcare Numbers etc.</li></ul>

If your plan includes anonymization, you can toggle it with a checkbox in the Project settings during the upload process:

![Screenshot 2022-06-01 at 15.29.47.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/blpNp6zjqw0)

Note that the anonymization process *cannot be undone* as only the anonymized data is stored on Caplena.

The PII is replaced by placeholders indicating what kind of PII has been removed:

![Screenshot 2022-06-01 at 15.35.41.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/7MS4c2V5Lqw)

## Languages and Translations

Anonymization operates on the source text and is performed **before** translation. This means that if the source text was anonymized, the translated text will be anonymized too. However, not all languages are supported for anonymization. Here's a list of supported languages:
* English
* French
* German
* Italian
* Korean
* Portuguese
* Russian
* Spanish
* Arabic
* Bulgarian
* Bengali
* Catalan
* Croatian
* Czech
* Danish
* Dutch
* Greek
* Finnish
* Hebrew
* Hindi
* Hungarian
* Latvian
* Lithuanian
* Norwegian (Bokmål)
* Persian (Farsi)
* Polish
* Romanian
* Slovak
* Slovenian
* Swedish
* Tagalog
* Turkish
* Ukrainian

Texts in other languages will be not or only partially anonymized. We'll add more languages in upcoming releases.