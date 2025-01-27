---
stoplight-id: arvuzpx6y2gm3
---

## Find solutions for common questions

### What Language Should I Use for Topic Collections in Caplena?

Caplena is multilingual and can handle topic collections in any language we support. Essentially, the topic collection language should be the language in which you want to analyze your data.

If your project contains responses in different languages, we recommend enabling translation. This ensures all responses will be translated into the language set for your topic collection, providing consistency in analysis.

The selected topic language will also be used for chart labels when creating visualizations. 

For more information about languages and translation, please see [**this article**](09-01-Languages.md).


### Can I analyze data from multiple markets/countries in a single project?
Yes, we recommend analyzing all markets within a single project rather than setting up multiple projects. It simplifies the process and allows for more efficient management of data.

If your responses are in different languages, you can enable automatic translation. This allows you to create a single topic collection and analyze everything in one language, streamlining the process across all markets.

By using automatic translation and keeping everything in one language, you can apply the same topic collection across all markets.

You can create a dashboard to view and compare data by market/country, which provides deeper insights into each region.

For more information about languages and translation, please see [**this article**](09-01-Languages.md).

### What if I forgot to enable translations in Settings?

If you forgot to enable translations, you won’t be able to activate it on your end after setting up the project. However, you can contact the Caplena Support Team, and we’ll enable the translation feature for you. Once it’s turned on, the system will translate the responses, allowing you to analyze everything in a single language.

For additional information on languages and translation, check [**this article**](09-01-Languages.md).

### Why am I getting an error saying "unable to cast column to number" when trying to upload additional data?

This error usually occurs when the order of the columns in the file you're uploading doesn’t match the data already on the platform. The columns need to be in the exact same order. You can check the data structure by looking under "Add Filter" in the "Additional Columns" section, or export your existing data to compare and see if anything is missing.

If you're still unable to upload the additional data, feel free to send the data file to our support team for a quick review.

For additional information on how to upload additional columns, check [**here**](12-Data-Manipulations.md).


### I need to restart analysis. Will my credits be charged again?
If you need to restart the analysis, your credits will not be charged again for the same data. Caplena only charges credits when you first upload and analyze the data. Once the data is in the system, you can rerun the analysis, change topics, or make adjustments without being charged additional credits.

To learn more about credits, click [**here**](03-05-Credits.md).

### How can I share a dashboard with a colleague or client?

There are two ways to share dashboards in Caplena:

**Sharing Internally (Collaboration)**

**Ideal for cases when your colleagues need to collaborate on the dashboard.**

To share a dashboard internally:
- Go to Dashboards.
- Select the dashboard you want to share.
- In the top-right corner, click the two-person icon to modify permissions and share with your team.

![Screenshot 2024-09-25 at 17.00.27.png](<../assets/images/Screenshot 2024-09-25 at 17.00.27.png>)


**Sharing Externally (View-Only)**

**Best for cases when recipients only need to review results without the ability to make changes.**

To share a dashboard externally:

- Open the dashboard.
- In the top-right corner, enable the shareable link option.
- Copy the link (with or without predefined filters) and share it with the intended recipient.
![Screenshot 2024-09-25 at 16.58.34.png](<../assets/images/Screenshot 2024-09-25 at 16.58.34.png>)

For more insights into dashboards, please follow [**this link**](07-02-Creating-Dasboards.md).

### What if my data file has cells marked as "N/A" or other placeholder values instead of being empty?
 If cells contain placeholder text like “N/A” or “-99,” they will be recognized as responses and will be billed. To prevent this, you can either delete these values or set them as Dummy Values in your account settings.

 In your **Account Settings**, go to the **Dummy Value section**, where you can enter up to three dummy values (e.g., “N/A,” “-99”). Caplena will ignore these values during analysis, so they won’t count toward billing.

 ![Screenshot 2024-11-04 at 16.52.13.png](<../assets/images/Screenshot 2024-11-04 at 16.52.13.png>)


By following these steps, you can ensure that only meaningful responses are billed while avoiding charges for placeholders or empty cells.

### What to do if I cannot upload a file or keep getting network error

 **Why can't I upload files or keep getting network errors?**
This may be due to network restrictions, browser issues, or firewall settings.

**What domains should I whitelist?**

Whitelist the following to ensure access:

1. caplena.com
2. *.caplena.com (all subdomains)


**Could my browser be causing the issue?**

Yes, try:

- Clearing cache and cookies
- Using a different browser (Chrome, Firefox)
- Disabling browser extensions

**Can VPNs or proxies cause problems?**

Yes, they might interfere. Disable them temporarily and try again.

**How do I check if my firewall is blocking uploads?**

Consult your IT team to whitelist Caplena and test by temporarily disabling security software.

**What if the issue persists?**

Contact Caplena support with details of the error and troubleshooting steps taken





### Why do the percentages in the charts exceed 100%?
The percentages can add up to more than 100% because a single feedback entry can belong to multiple categories. For example, if a user mentions both "Communication & Information" and "Processes" in their response, that feedback is counted in both categories. This approach allows for a more detailed and accurate analysis of feedback across various topics.

 **Should I be concerned about totals exceeding 100%?**

No, this is expected behavior. It reflects the overlapping nature of feedback distribution and provides a comprehensive view of how user comments are categorized. Rather than focusing on the total percentages, it’s better to interpret the data category by category to understand how frequently each topic is mentioned.