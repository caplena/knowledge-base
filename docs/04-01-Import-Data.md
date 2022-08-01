---
stoplight-id: 85eh1l8jcavy0
---

# Data Import

## Import Options
Importing data into the Caplena platform is the first step to start a new project. After clicking on the *New Project* or *Import Data* button you will be able to choose between three data import options.

![Bildschirmfoto 2022-07-01 um 20.09.55.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/XPVSgepPBtE)

### Upload a File
Using this option, you can simply drag and drop your data file into the import box or browse to the location of your file. The currently supported data formats for this import option are: .xls, .xlsx, .csv, .txt, .spss and .sav.

#### Data Structure
The data should be arranged in columns and rows, where the rows include the indiviudal records such as respondends, reviews or social media feedback.

The first row of the data file will be treated as the column header or title. In case you have the description of your data columns across several rows, e.g., the variable name in the first row and a description the second, you should delete one of these rows or merge them into a single row.

#### Additional Data
Together with your text to analyze you can upload additional data columns with text and / or numerical data, such as age, gender, NPS-scores etc. These additional data columns will not be analyzed as text and you will not be charged for them. However, we recommend uploading additional data columns as you can use them as segmentation or filter variable and they can also be display besides your text when fine-tuning.

### Direct Input
You can also enter or copy your data directly into the upload window. The lines will be separated by pressing enter. When copying the data directly from Excel or a similar application, the data will be line-separated automatically.

![Bildschirmfoto 2022-07-01 um 20.10.46.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/07h8s0WTwwo)


### Integrations
The third and last option to import data to analyse with Caplena is the direct integration of external data sources, which are mainly customer reviews from various customer review websites, such as Amazon, Trustpilot, Google Maps etc.

Here you can select reviews for one or several products, services, locations (shops, restaurants, hotels, etc.) or software applications by copying the URL or a similar unique identifier to start with the data import.

Currently available sources for customer reviews / integrations are as follows:

![Bildschirmfoto 2022-07-01 um 20.10.23.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/AHcDoFsiVgg)


For each external data source you will find a guideline on how to identify the reviews that you would like to analyze. In most cases it is as simple as copying the URL, just click on any of the logos in your [Upload](https://caplena.com/app/upload) section and follow the steps behind it.

Please also have a look at our more detailed article on our integrations feature: [Integrations in Detail](docs/04-09-Integrations-in-Detail.md)

The following tutorials show the Integrations features in practice:
- A case study comparing two meditation apps - [Click here](https://blog.caplena.com/2021/08/25/headspace-vs-calm-a-comparative-analysis-of-customer-reviews/)
- Tutorial walk-through taking the Netflix app as an example - [Click here](https://blog.caplena.com/2020/05/06/walk-through-analyzing-open-ended-feedback-a-3-step-video-tutorial-on-netflix-app-reviews/)

## Multiple Text Columns
When starting a project, you have either a single column with text to analyze or you have several text columns in one row. The latter is often true when analyzing survey data with several open-ended questions.

### A Single Column
In case you are analyzing the answers to a single open-ended question from a survey, reviews from a customer review website (such as Google Maps, Apple App Store, Amazon, etc.) or social media feedback, you will have a project with a single text-column. Thus, you simply upload your open-ended data together with your auxiliary data columns (these can be any additional variables such as ID, ratings, demographics, dates, countries, etc.) that you like to use for analysis, filtering, and segmentation.

### Multiple Columns
When analyzing survey data, you might have more than one open-ended question in your questionnaire. In such cases, you do not have to create several individual projects to analyze them across different individual projects. Instead, you can import your data all at once as a single file.

The example below includes two open-ended questions as well as several auxiliary variables for analytical purposes.


![Bildschirmfoto 2022-05-13 um 10.58.48.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/Hvv5D2d33vs)

Using this approach makes only sense when you have your data organized like in the example above, i.e., in one sheet in which each row represents one respondent.

Despite having all questions within one project, the actual analysis will take place on an individual text level. All text columns / questions will be shown when accessing your project.

## Add More Text-Data

You may have already started or finished the analysis for your project, but you would like to add more data, be it from a new or previous wave or from an additional market and the like.

You can add new data to your project any time by using the *Upload further answers* feature that you will find at the top menu when selecting your project from the [Project View](https://caplena.com/app/projects).

![Bildschirmfoto 2021-12-30 um 12.20.58 v2.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/sTNZT74J4I0)

Provided your existing data has already been analyzed, i.e., topic collection was applied, the newly added data will be automatically assigned with topics based on the existing topic collection.

This procedure can be repeated as many times as you wish.

### Data Structure

The additional data should be arranged in the same way as the original data, i.e., it should have the **same number of data columns** and they should be **arranged in the same order**. The data rows can be in any order.

### Auto-Translation

In case you would like to use our auto-translation feature, please **enable it when you initially create your project**. It is not possible to enable this feature retrospectively when uploading additional data to an existing project with no auto-translation enabled. Learn more about [auto translation](04-02-Languages-Supported.md#automatic-translations).

### Duplicate Row Handling

A row of data is considered to be a duplicate if all values in all columns are exactly equal. By default, duplicates will be ignored and not be imported. However, in case you would like to disable this feature, you can simply turn of the *Skip existing* function in the *Match your data* view (see screen shot below).

**De-duplicate rows by ID-number**: Optionally, and as an alternative to the above, you can choose a column with unique values only (such as an ID-number) to identify already existing rows. If no ID column is selected, rows are identified following the rules described in the previous paragraph.

![Bildschirmfoto 2022-01-03 um 16.29.09.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/6zKTyTsgu4Y)

## Leverage Non-Text Data
When uploading a project to Caplena, all columns you do not select to be processed as text, will be treated as additional columns and uploaded to the platform nevertheless.

This data could be metadata of the respondent (age, gender, customer segment, country, etc.), an ID column for later identification in the export, or responses to closed-questions such as a likelihood to recommend question (NPS score).

<!-- theme: info -->

> To benefit most from Caplena, we recommend adding as many relevant additional columns as possible.

### Visualization

Text

