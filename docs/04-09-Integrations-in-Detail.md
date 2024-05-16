---
stoplight-id: 2784zjo1mosah
---

# Integrations in Detail

## What are Integrations?

Integrations can be used to import answers from third-party platforms and analyze them directly within Caplena. There are multiple integrations to choose from, and currently, a broad range of review platforms (for an overview of all integrations, click here) is supported. For every integration that the user adds, exactly one Caplena project is created, which contains the imported answers from the third-party platform. Thus, an integration acts as a data source for a single project.

### Integration Items
An integration item is a resource that contains answers to be analyzed (e.g. reviews for an app in the Google Play Store). Every integration can consist of multiple integration items from which the answers are fetched from. 

To make the distinction between integrations and integration items more clear, let us consider an example where we are trying to compare what customers think about different gaming consoles. For this, we create a new Amazon integration that contains two integration items, namely the reviews for the PlayStation 5 and Xbox Series X consoles. Out of this integration, a single project that containing the reviews for both consoles is created - as can bee seen in the image below.

![Bildschirmfoto 2022-07-01 um 20.05.24.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/nZs8T4AMjk0)


## Synchronization

One of the biggest advantages of using integrations is the synchronization feature. With synchronization enabled, new answers submitted to an integration item will be uploaded to the respective project automatically.

The sync process is always triggered at 2:00 AM UTC, and can take anywhere from a few minutes to a few hours to complete successfully. The synchronization can be disabled within the project settings, but please be aware that due to technical limitations, re-enabling synchronization after it has been disabled for more than 5 days is not possible for all review platforms supported by us. 

Coming back to our gaming console comparison; assuming that daily sync is enabled, new reviews for both the PlayStation 5 and Xbox Series X will be imported into the respective Caplena project every single day without any manual user interaction.

## Billing

Using the integration feature does not incur any additional costs - **every text element costs just one credit** ([click here](03-05-subscriptions-and-billing.md) to learn more about our credit system) and those credits will be **deducted from your account during upload**. No credits will be deducted **as long as you don't save** the project. If synchronization is enabled, you will be billed for the number of **appended text elements accordingly**.

To make it easier for you to estimate how many credits an integration will cost, we display the estimated number of responses for every integration item. In our previous example, we estimated a total of 19822 reviews for the PS5 and 7979 reviews for the Xbox Series X.

<!-- theme: info -->
> Please note: The count displayed is only an estimate, so oftentimes the actual number imported is much smaller (but it might also be larger on rare occasions). You will only be billed for the amount answers that were actually imported!

Let us consider a few examples to make things more clear:

**Example 1**: You create an integration with three Amazon products that each have 1000 reviews at that point. In the Organize view, you select exactly one question, marking the other columns as auxiliaries. Every day, 10 new reviews are submitted for each product, and you have daily synchronization enabled. Since you only have one question, this costs you `3 * 1000 = 3000` credits when the project is created and a further `3 * 10 = 30` credits every single day (as long as you don't disable the sync).

**Example 2**: You create an integration with three Capterra businesses and each has 1000 reviews. In the Organize view, you select the review text itself and the job title as questions. In the project settings, you disable the synchronization. Since you now have two questions, this will cost you `2 * 3 * 1000 = 6000` credits when the project is created and no further credits are deducted since sync is disabled.

## Supported Integrations

As of right now, our integrations feature allows you to import and synchronize reviews from across eight different platforms. We've listed them below, showing how you can use these for generating your own insights.

### Google Maps

Input Format: `<name>, <address>, <country>`

In general, you should try to specify the address to the venue as detailed as possible by combining the name, address and country. For example, let us consider the *WERK 8* restaurant as shown in the image. We should end up with the following input: 

`WERK 8, Dornacherstrasse 192, 4053 Basel, Switzerland`

![Bildschirmfoto 2022-07-01 um 20.01.52.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/laX2mNByrWE)

**Examples:**

`WERK 8, Dornacherstrasse 192, 4053 Basel, Switzerland`  
`The Newark Museum of Art, 49 Washington St, Newark, NJ 07102, United States`  
`Kunsteisbahn Margarethen, Im Margarethenpark 10, 4053 Basel, Switzerland`

### Trustpilot

Input Format: `https://www.trustpilot.com/review/<domain>`

**Examples:**

`https://www.trustpilot.com/review/buzzsprout.com`  
`https://www.trustpilot.com/review/www.smtp2go.com`  
`https://www.trustpilot.com/review/cyberghostvpn.com`

### Apple App Store

Input Format: 

- Default Region (US): `https://apps.apple.com/app/<name>/<identifier>`
- Custom Region: `https://apps.apple.com/<region>/app/<name>/<identifier>`
   - Supported regions: `ca`, `at`, `it`, `us`, `au`, `fr`, `ch`, `mx`, `es`, `de`

**Examples:**

`https://apps.apple.com/app/1password-7-password-manager/id1333542190`  
`https://apps.apple.com/app/omnigraffle-7/id1142578753`  
`https://apps.apple.com/app/bear/id1091189122`  
`https://apps.apple.com/de/app/fifa-soccer/id1094930513`  

### Google Play Store

Our integration for Google Play Store support fetching reviews for apps, books and even movies. Depending on what type of resource you want to fetch, a different input format is being used. Google Play Store displays different reviews depending on the language set in the URL.

Input Format:

- Apps: `https://play.google.com/store/apps/details?id=<app-bundle>&hl=(fr|de|en|it|es|pl|nl)`
- Movies: `https://play.google.com/store/movies/details/<name>?id=<identifier>`
- Books: `https://play.google.com/store/books/details/<name>/?id=<identifier>`

The `hl` parameter defines the language of the reviews. If you do not set this parameter, value en is used. Note that the language is not reliable and reviews in other languages may appear. To fetch all reviews that exist for a given project you need to add a separate URL for every value of `hl`.

**Examples**:

- Apps  
  `https://play.google.com/store/apps/details?id=ch.admin.babs.alertswiss&hl=de`  
  `https://play.google.com/store/apps/details?id=org.coursera.android`  
  `https://play.google.com/store/apps/details?id=com.pluralsight`  

- Movies  
  `https://play.google.com/store/movies/details/Fast_Furious_8?id=s60g2-Fxfn4`  
  `https://play.google.com/store/movies/details/Wolf_of_Wall_Street?id=SpIJBP8XtXk`  
  `https://play.google.com/store/movies/details/Bohemian_Rhapsody?id=myGzyVRZhzU`

- Books  
  `https://play.google.com/store/books/details/Albert_Einstein_The_World_as_I_See_It?id=Y_9kDwAAQBAJ`  
  `https://play.google.com/store/books/details/Tzu_Sun_The_Art_of_War?id=WeHsAQAAQBAJ`  
  `https://play.google.com/store/books/details/James_S_A_Corey_Babylon_s_Ashes?id=MzA9CgAAQBAJ` 

### Amazon

As of right now, we support five different Amazon stores, namely `amazon.com`, `amazon.fr`, `amazon.de`, `amazon.it` and `amazon.co.uk`. In addition, we support two different URL formats, one with and one without name.

Country Identifiers: `com`, `fr`, `de`, `it`, `co.uk`, `es`, `ca`, `com.au`, `in`, and `co.jp`

Input Format: 

- with name: `https://www.amazon.<country>/<name>/dp/<ASIN>`
- without name: `https://www.amazon.<country>/dp/<ASIN>`

The Amazon Standard Identification Number or [ASIN](https://en.wikipedia.org/wiki/Amazon_Standard_Identification_Number) is the unique product identfier used by Amazon.

**Examples:**

- with name:  
  `https://www.amazon.com/First-Years-Stack-Up-Cups/dp/B00005C5H4/`  
  `https://www.amazon.fr/Nero-Giardini-P805261D-Sneakers-Femme/dp/B08V5KPJVN`  
  `https://www.amazon.de/Colgate-Charcoal-Whitening-Zahnpasta-Zahnbürste/dp/B088VCM63D`  
  `https://www.amazon.it/Ray-Ban-0RB3447N-Occhiali-Crystal-Grad-Blue/dp/B076VNZK4V`  
  `https://www.amazon.co.uk/Pinch-Nom-Everyday-Light-Slimming/dp/1529026407`

- without name:  
  `https://www.amazon.com/dp/B00WBJGUA2`  
  `https://www.amazon.fr/dp/B01N9BU4Y7`  
  `https://www.amazon.de/dp/B086DKVS1P`  
  `https://www.amazon.it/dp/B07NQDHC7S`  
  `https://www.amazon.co.uk/dp/B08KGTW3CV`  

### G2

Input Format: `https://www.g2.com/products/<name>/reviews`

**Examples:**

`https://www.g2.com/products/clickup/reviews`  
`https://www.g2.com/products/dotpeek/reviews`  
`https://www.g2.com/products/sentry/reviews`


### Capterra

Input Format: `https://www.capterra.com/p/<identifier>/<name>/`

**Examples:**

`https://www.capterra.com/p/46497/QuickBooks/`  
`https://www.capterra.com/p/177841/NetSuite/`  
`https://www.capterra.com/p/138689/Booqable/`


### Yelp

Input Format: `https://www.yelp.com/biz/<name>`

**Examples:**

`https://www.yelp.com/biz/franchia-vegan-cafe-new-york`  
`https://www.yelp.com/biz/tibits-basel`  
`https://www.yelp.com/biz/brandenburger-tor-berlin`

### Brandwatch

Our Brandwatch integration simplifies the process of importing social media query results directly into Caplena for analysis. Here's how you can set it up:

1. **Accessing Account Settings:** Start by accessing your Caplena account settings. Navigate to "Integrations" and select Brandwatch.
![Screenshot 2024-04-10 at 16.39.06.png](<../assets/images/Screenshot 2024-04-10 at 16.39.06.png>)

2. **Adding Brandwatch Account:** Click on the "Add Account" button. Fill in the required details including the connection name, username, password, and your project name. **Please note** that you can find the project name in your Brandwatch account.

![Screenshot 2024-04-10 at 16.43.13.png](<../assets/images/Screenshot 2024-04-10 at 16.43.13.png>)

3. **Connecting Account:** Once you've filled in the details, click on "Connect Account" to finalize the setup.

![Screenshot 2024-04-10 at 16.26.38.png](<../assets/images/Screenshot 2024-04-10 at 16.26.38.png>)


4. **Importing Data:** With the setup complete, you can now import your data. Navigate to "Projects" in Caplena, click on "Import Data", and select Brandwatch from the integration list. Choose the account and query from which you'd like to import your data.

![Screenshot 2024-04-10 at 16.51.57.png](<../assets/images/Screenshot 2024-04-10 at 16.51.57.png>)

Here's a quick video demonstrating all the steps mentioned above:

https://youtu.be/qEtocKmrBbY

### Qualtrics

Integrating Qualtrics with Caplena enables efficient analysis of qualitative data collected through Qualtrics surveys. This integration streamlines the entire process from data collection to insights generation, offering a comprehensive view of survey results.

To connect Qualtrics with Caplena, follow these steps:
1. **Access Account Settings**
2. **Select Integrations** (at the bottom of the menu list)
3. **Select Qualtrics** (from the list showing at the top right)

![Screenshot 2024-05-13 at 17.16.25.png](<../assets/images/Screenshot 2024-05-13 at 17.16.25.png>)


The next step would be to fill in the following fields:

![Screenshot 2024-05-14 at 11.11.18.png](<../assets/images/Screenshot 2024-05-14 at 11.11.18.png>)

* **Connection name** - The "Connection Name" is a label you assign to your integration setup for easy identification. Choose a name that makes sense to you and helps distinguish this specific integration from others you may have set up.

* To locate **the API Key** for your Qualtrics account, follow these steps:

1. Log in to your Qualtrics account.
2. Navigate to Account Settings.
3. Select "Qualtrics IDs" 
4. Look for the API section, where you will find your API Key.

* To find **the Datacenter information** for your Qualtrics account, follow these steps:
1. Log in to your Qualtrics account.
2. Go to Account Settings.
3. Look for the "Qualtrics IDs" 
4. You'll find the Datacenter under the User section

![Screenshot 2024-05-14 at 12.10.57.png](<../assets/images/Screenshot 2024-05-14 at 12.10.57.png>)

You are all set now and you can create your project. Click on [Import Data / New Project](https://caplena.com/app/upload), and select Qualtrics from the list of integrations under "Connected Accounts".

![Screenshot 2024-05-14 at 13.22.38.png](<../assets/images/Screenshot 2024-05-14 at 13.22.38.png>)

Choose the account and survey from which you'd like to import your data.


![Screenshot (28).png](<../assets/images/Screenshot (28).png>)













