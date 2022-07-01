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

One of the biggest advantages of using integrations is the synchronization feature. With synchronization enabled, new answers submitted to an integration item will be uploaded to the respective project automatically. You can choose between three different synchronization intervals (daily, weekly or monthly) or even disable the synchronization completely. 

The sync process is always triggered at 2:00 AM UTC, and can take anywhere from a few minutes to a few hours to complete successfully. It is also possible to change the synchronization interval directly from the project settings, making it possible to disable the feature when not needed. Please note that due to technical limitations, re-enabling synchronization after it has been disabled for more than 40 days is not possible for all review platforms supported by us. 

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

In general, you should try to specify the address to the venue as detailed as possible by combining the name, address and country. For example, let us consider the WERK 8 restaurant as shown in the image. We should end up with the following input: 

`WERK 8, Dornacherstrasse 192, 4053 Basel, Switzerland`

![Bildschirmfoto 2022-07-01 um 20.01.52.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/laX2mNByrWE)

`WERK 8, Dornacherstrasse 192, 4053 Basel, Switzerland` _`The Newark Museum of Art, 49 Washington St, Newark, NJ 07102, United States`_

`Kunsteisbahn Margarethen, Im Margarethenpark 10, 4053 Basel, Switzerland`

