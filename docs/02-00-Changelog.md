---
stoplight-id: 7d800a323b890
---
# Changelog
---

## 2024-10-08
* Improved information on mismatching columns when appending rows
* Fixed bug with dashboard editing permissions when switching verbatim element from "Show Rows" to "Show Summary"
* Fixed issues when adding multiple verbatim elements with the summary on

## 2023-09-08

### Upload
* Improved accuracy of __source language detection__ in translation logic (resulting in better translations)
* Fixed bug in qualtrics integration sending out multiple messages of integration succeeding/failing

### Row deletion
* Added capability to remove rows in the fine-tuning view


### Account
* Aggregating credit usage on daily basis to have cleaner usage statistics when importing via API





## 2023-07-14

### AI Quality Score revamped

* Score is now available even without manual reviews
* Fluctuates significantly less across AI updates

### Summary feature

* Extending number of rows considered in summarization 


## 2023-06-23

### Charting & Dashboarding
* Fixed issues with weighting in NPS gauge chart

### Upload
* Improved DeepL translation by automatically falling back to Google Translate for languages not supported by DeepL


## 2023-05-11

### Charting & Dashboarding

* Performance improvements on large dashboards
* Fixed filters for charts with data from multiple projects

### API
* Sunset of v1 API

## 2023-04-21

### Charting & Dashboarding

* Added additional date filters for last 3 months and last 12 months
* Improve filtering display in row browser

### Upload

* Fixed required credits display for review and other integrations
* Improved stability of qualtrics integration

## 2023-02-27

### Charting & Dashboards

* Improved filtering for multiple select
* Added sample size indication to all charts
* Enable copying additional values from chart row browser

### Topic assignment

* Adjusted behaviour of topic selection dropdown for long text with many topics

## 2023-01-27

### Charting & Dashboards

* Fixed issue in dashboard filtering via shareable link
* Resolved problems with saving colors and custom scoring ranges in charts
* Re-enabled filtering "Verbatim Sample" in dashboards
* Fixed Date Line&Pie Chart legend problems

### Upload and Export
* Added handling of carriage return in Excel uploads (leading to _X000D_ in the text)
* Enforcing limit of 200'000 maximum rows downloadable via v1 API

---

## 2022-12-22

* Added Admin role to Business and Freelance plans. The Admin role allows inviting new users to Caplena and managing the subscription
* Additional chart previews are now available in the question cockpit
* Simplified "Organize" step in Upload and clarified credit deduction

---

## 2022-12-11

* New comparison bar chart allowing exploring differences between segments and the overall value

---

## 2022-11-18

### Charting & Dashboards
* Added segment size indication "(n=...)"
* Fixed issue with bar labels remaining visible when deselecting series from the legend
* Fixed coloring issue in driver chart

---

## 2022-11-15

* Fixed incorrect relative impact values in Driver Chart Excel export with sentiment topics
* Fixed counts in NPS Gauge chart being incorrectly displayed if scoring ranges had no matching rows
* Performance improvements for bulk update

---

## 2022-11-09

### Charting & Dashboards
* Simplified Relationship Graph for Topics with sentiment
* Enabled Excel Export for Relationship Graph
* Fixed date filtering on "All Time"
* Enabled embedding Dashboards as iFrames in other applications

### Integrations and Upload
* Fixed issues with Review integrations
* Improved handling of multiple columns with language identifiers
* For the anonymization feature: Added additional languages (including Thai and Japanse) plus improved the accuracy on existing languages.



