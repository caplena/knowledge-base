---
stoplight-id: waiokjkj9al83
---

# Anonymize Text Comments

Caplena can automatically remove the following personal identifiable information (PII) from all text comments. This ensures your data remains compliant with privacy standards and safe for further processing.

If your plan includes anonymization, you can toggle it in the Project settings:

![Screenshot 2025-03-27 at 11.43.51.png](<../assets/images/Screenshot 2025-03-27 at 11.43.51.png>)

When you you click Continue, you can select which types of information you'd like to anonymize—such as email addresses, phone numbers, or usernames. Simply check the relevant boxes in the Anonymization Settings panel.

For more granular control, expand the Advanced Settings section. This allows you to:

- Anonymize additional PII types (e.g., Date of Birth, ZIP Code, Religion, Gender, etc.)
- Define sensitive data fields that aren’t covered by default
- Tailor anonymization to your industry or compliance requirements

![Screenshot 2025-03-27 at 11.47.59.png](<../assets/images/Screenshot 2025-03-27 at 11.47.59.png>)

📝 **Allow-List**

Need to retain specific terms (like brand names or product models)? Use the Allow-list to exclude them from anonymization.

- Click “Add term”
- Paste a list from Excel to bulk-add
- Matching is case-insensitive

Once you've selected the settings that match your needs, click Continue to move forward with your data import or processing.


>Note that the anonymization process *cannot be undone* as only the anonymized data is stored on Caplena.

The PII is replaced by placeholders indicating what kind of PII has been removed:

![Screenshot 2025-03-27 at 12.11.45.png](<../assets/images/Screenshot 2025-03-27 at 12.11.45.png>)


The anonymization process takes place right after the upload onto the Caplena server. The original data - the data that includes the PII information – will not be visible at any time. For technical reasons, the original data that includes the PII information will remain on the Caplena server for a short period of time, before it will be automatically and permanently deleted from the server and its backup system.

### Anonymization Tips

📍 **Address vs. Location**

**Address** refers to structured location formats: street name, house number, ZIP/postcode, and city
(e.g., “25 Oxford Street, London W1D 2LF” or “742 Evergreen Terrace, Springfield, IL 62704”)

**Location** captures general geographic mentions or landmarks
(e.g., “Central Park”, “the Lake District”, “Northern California”)

![Screenshot 2025-05-19 at 09.38.54.png](<../assets/images/Screenshot 2025-05-19 at 09.38.54.png>)


**🧭 Address vs. Street/City/ZIP/Postcode**


![Screenshot 2025-05-16 at 18.03.27.png](<../assets/images/Screenshot 2025-05-16 at 18.03.27.png>)


Use these settings if you'd like to partially anonymize geographic information (e.g., preserve city names but remove street-level data).

🔢 **What is Numerical PII?**
Numerical PII includes numeric identifiers not covered by other fields like credit cards or account numbers.

![Screenshot 2025-05-16 at 18.06.10.png](<../assets/images/Screenshot 2025-05-16 at 18.06.10.png>)


🏢 **Organization vs. Occupation**

![Screenshot 2025-05-16 at 18.10.21.png](<../assets/images/Screenshot 2025-05-16 at 18.10.21.png>)

> There is no separate “Company” field — company names are anonymized using the Organization setting.

🛑 Important to Know
Anonymization cannot be undone once applied to a project.

If you anonymize more than intended, you’ll need to reupload the data into a new project.

If you make a mistake, just reach out to us — we’re happy to help and will reimburse credits if needed.



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