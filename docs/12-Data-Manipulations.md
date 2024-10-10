---
stoplight-id: ghwl4n1vzazqu
---

# Data Manipulations

* [Append Rows to existing project ](#append-rows)
* [Add, remove, and edit columns ](#add-remove-edit-columns)

## Append Rows to existing project
You may have already started or finished the analysis for your project, but you would like to add more data, be it from a new or previous wave or from an additional market and the like.

You can add new data to your project any time by using the *Upload further answers* feature that you will find at the top menu when selecting your project from the [Project View](https://caplena.com/app/projects).

![Bildschirmfoto 2021-12-30 um 12.20.58 v2.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/sTNZT74J4I0)

Provided your existing data has already been analyzed, i.e., topic collection was applied, the newly added data will be automatically assigned with topics based on the existing topic collection.

This procedure can be repeated as many times as you wish.

### Data Structure

The additional data should be arranged in the same way as the original data, i.e., it should have the **same number of data columns** and they should be **arranged in the same order**. The data rows can be in any order.

### Auto-Translation

In case you would like to use our auto-translation feature, please **enable it when you initially create your project**. It is not possible to enable this feature retrospectively when uploading additional data to an existing project with no auto-translation enabled. Learn more about [auto translation](09-01-Languages.md#auto-translation-in-detail).

### Duplicate Row Handling
A row of data is considered to be a duplicate if all values in all columns are exactly equal. By default, duplicates will be ignored and not be imported. However, in case you would like to disable this feature, you can simply turn of the *Skip existing* function in the *Match your data* view (see screen shot below).

**De-duplicate rows by ID-number**: Optionally, and as an alternative to the above, you can choose a column with unique values only (such as an ID-number) to identify already existing rows. If no ID column is selected, rows are identified following the rules described in the previous paragraph.

![Bildschirmfoto 2022-01-03 um 16.29.09.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/6zKTyTsgu4Y)


## Add or Replace Additional Columns
Sometimes, during project work, you may find the need to

* add additional data columns
* update existing data within the additional columns
* delete additional columns imported initially

This can be achieved using the **add or replace additional columns** feature which is part of the *Project Actions* (the icon showing a pair of scissors), the menu at the top right when opening any project from the *Project List*.

 ![Bildschirmfoto 2024-02-08 um 16.37.00.png](<../assets/images/Bildschirmfoto 2024-02-08 um 16.37.00.png>)

<!-- theme: info -->

> Note: This feature concerns any additional column, i.e., the columns that can be used as filter and for segmentations. Text columns will not be affected!

**In short the feature / process works as follows.**

1. Make your changes offline in the original data file
2. Select the “Add or replace” feature from the *Project Actions*
3. Drop your file
4. Check and confirm changes in the *Match Columns* view

The individual steps in detail.


### Data File Preparation
Use the data file you used for your initial import and make the required changes in that same file, i.e., delete columns, add columns, or make changes to any of the additional columns.

Make sure that the data is in the same order as it is on the platform. If in doubt or in case you have already added several waves of data, you can always export the file from the platform and make the changes in that file. This ensures you have all the data in one file and the records are in the same order as in Caplena.

**Follow these steps when using a file exported from Caplena.**

* Delete all coding information and metadata (such as review status, text highlight information, etc.) as well as the two nested rows at the top that indicate the column sections.
* Also remove the text to analyze column, the text columns will not be effected.

The file in which you will do your changes should only contain the additional columns in the order of initial import.

![Bildschirmfoto 2024-02-08 um 16.13.35.png](<../assets/images/Bildschirmfoto 2024-02-08 um 16.13.35.png>)

Apply your changes to this file.

<!-- theme: warning -->
> #### Check numerical columns when exporting Excel files
>
> When exporting data in Excel format it can happen that epmpty cells in numerical columns are filled with a place holder such as #NUM or #ZAHL. Please check and replace with an empty value before the re-import. This can be avoided when exporting the data in CSV format.

### File Import
Navigate to your *Project List* and open the project which you would like to change. Select **add or replace** from the *Project Actions* and drop the file with the changes. 

After dropping the file the *Match Columns* screen will allow you to review your changes before being applied. The Summary at the bottom right will show the number of
* Columns present previously  and in new file
* Columns not present anymore in new file
* New columns

Move your mouse overt the information icon next to each of the three items and the column names will be shown.

When the proposed changes match your expectation click on **Replace & Save**, the blue button on the bottom right. Your data file will be imported, and the changes will be applied. You will be able to see and use the changed set of additional columns as filter and for segmentation.

