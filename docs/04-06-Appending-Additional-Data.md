---
stoplight-id: m3j25nsa9fe3k
---

# Appending Additional Rows to an Existing Project

You may have already started or finished the analysis for your project, but you would like to add more data, be it from a new or previous wave or from an additional market and the like.

You can add new data to your project any time by using the "Upload further answers" feature that you will find at the top menu when selecting your project from the [Project View](https://caplena.com/app/projects).

![Bildschirmfoto 2021-12-30 um 12.20.58 v2.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/sTNZT74J4I0)

Provided your existing data has already been analyzed, i.e., topic collection was applied, the newly added data will be automatically assigned with topics based on the existing topic collection.

This procedure can be repeated as many times as you wish.

## Data structure

The additional data should be arranged in the same way as the original data, i.e., it should have the **same number of data columns** and they should be **arranged in the same order**. The data rows can be in any order.

## Auto-Translation

In case you would like to use our auto-translation feature, please **enable it when you initially create your project**. It is not possible to enable this feature retrospectively when uploading additional data to an existing project with no auto-translation enabled.

## How duplicate rows are handled

A row of data is considered to be a duplicate if all values in all columns are exactly equal. By default, duplicates will be ignored and not be imported. However, in case you would like to disable this feature, you can simply turn of the "Skip existing" function in the "Match your data" view (see screen shot below).

**De-duplicate rows by ID-number**: Optionally, and as an alternative to the above, you can choose a column with unique values only (such as an ID-number) to identify already existing rows. If no ID column is selected, rows are identified following the rules described in the previous paragraph.

![Bildschirmfoto 2022-01-03 um 16.29.09.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/6zKTyTsgu4Y)
