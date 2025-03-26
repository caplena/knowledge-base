---
stoplight-id: yjzafq6ajslqt
---

# Append Rows to existing project

Need to add more responses to your existing Caplena project? You can easily do this right from the Data View tab.

Provided your existing data has already been analyzed, i.e., topic collection was applied, the newly added data will be automatically assigned with topics based on the existing topic collection.

This procedure can be repeated as many times as you wish.

1️⃣ **Go to the Data Tab**

In your project, click the data icon on the left-hand navigation bar.
Then, in the top right corner, click “Add new rows”.

![Screenshot 2025-03-26 at 14.45.43.png](<../assets/images/Screenshot 2025-03-26 at 14.45.43.png>)

2️⃣** Upload Your File**

In the import screen:

- Drag and drop your file or browse to upload
- (Optional) Give your data source a name to help you keep track
- Make sure your file includes column headers as the first row
- Click Continue to proceed

![Screenshot 2025-03-26 at 14.38.48.png](<../assets/images/Screenshot 2025-03-26 at 14.38.48.png>)

3️⃣ **Match Your Columns**

In the next screen, you’ll match the columns from your new file with the existing columns in the project.

✅ Caplena will automatically match columns with the same name

✅ Columns don’t need to be in the same order as before


 You can:

- Skip columns you don’t want to import
![Screenshot 2025-03-26 at 15.24.59.png](<../assets/images/Screenshot 2025-03-26 at 15.24.59.png>)

- Create new columns for unmatched data
![Screenshot 2025-03-26 at 15.23.54.png](<../assets/images/Screenshot 2025-03-26 at 15.23.54.png>)

- Manually match columns if automatic matching doesn’t work as expected

![Screenshot 2025-03-26 at 15.26.36.png](<../assets/images/Screenshot 2025-03-26 at 15.26.36.png>)
<!-- theme: info -->

> Note: Use filters at the top to view and match specific column types (text, numerical, date, etc.)


![Screenshot 2025-03-26 at 15.30.43.png](<../assets/images/Screenshot 2025-03-26 at 15.30.43.png>)




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


