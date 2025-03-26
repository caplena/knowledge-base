---
stoplight-id: yjzafq6ajslqt
---

# Append Rows to existing project

Need to add more responses to your existing Caplena project? You can easily do this right from the Data View tab.

As long as your existing data has already been analyzed (meaning a topic collection is in place), any newly added data will automatically be assigned to topics based on that existing setup.

You can repeat this process as often as needed.

1️⃣ **Go to the Data Tab**

In your project, click the data icon on the left-hand navigation bar.
Then, in the top right corner, click “Add new rows”.

![Screenshot 2025-03-26 at 14.45.43.png](<../assets/images/Screenshot 2025-03-26 at 14.45.43.png>)

2️⃣ **Upload Your File**

In the import screen:

- Drag and drop your file or browse to upload

>Please note that your data file no longer needs to have the same column order or number of columns as before.
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

4️⃣ **Validate and Finalize**

Once you’ve reviewed everything:

- Click Validate to confirm your mappings
- Then, finalize the upload process

![Screenshot 2025-03-26 at 15.41.00.png](<../assets/images/Screenshot 2025-03-26 at 15.41.00.png>)

Your new data rows will now be added to the existing project 🎉

### Auto-Translation

In case you would like to use our auto-translation feature, please **enable it when you initially create your project**. It is not possible to enable this feature retrospectively when uploading additional data to an existing project with no auto-translation enabled. Learn more about [auto translation](09-01-Languages.md#auto-translation-in-detail).

### Duplicate Row Handling
A row of data is considered to be a duplicate if all values in all columns are exactly equal. 

**De-duplicate rows by ID-number**: To avoid importing duplicates, enable the “Skip existing rows based on matched column” toggle at the top and select the column used for deduplication — usually an ID field.
This ensures that previously uploaded rows (based on a unique identifier) are not imported again.

![Screenshot 2025-03-26 at 16.07.34.png](<../assets/images/Screenshot 2025-03-26 at 16.07.34.png>)




