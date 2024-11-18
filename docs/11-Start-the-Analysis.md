---
stoplight-id: 5ykfg42sjns9x
---

# Start the Analysis / Initial Topic Generation
Once your data is in the project, you can start the analysis. Here we will explain the inital start of the analyis, which includes the selecting whether start afresh or make use of existing topics as well as the inital topic generation process.

Starting the analysis will be always the same process, no matter whether you imported a data file or whether you used an automatic import process such as review scraping (Google, Amazon, etc.), a connected account (Qualtrics, Zapier, etc.), or our API.

When you open your project, you will be directed to the Overview panel. Here, you will find the question designated for analysis, such as “Why did you give this rating?” in my case.

In this panel, you will also see an overview of potential topics identified in the dataset and an AI-generated summary. This summary offers insights into the main concepts mentioned, helping you quickly understand key points and trends within your data.

![Screenshot 2024-11-18 at 10.13.39.png](<../assets/images/Screenshot 2024-11-18 at 10.13.39.png>)


Once you're ready, you can click on the **Begin Analysis** button to create your topic collection.

![Screenshot 2024-11-18 at 10.58.17.png](<../assets/images/Screenshot 2024-11-18 at 10.58.17.png>)



## From Scratch or not?

**Starting Fresh**: Choose this option if you are analyzing this type of open text for the first time. The AI will review your text data and generate the initial categories and topics. To proceed, click on the Generate Topics button.

![Screenshot 2024-11-18 at 11.28.45.png](<../assets/images/Screenshot 2024-11-18 at 11.28.45.png>)


**Importing Existing Topic**s: If you already have a topic collection from previous work saved as an external file or from a prior Caplena project, select the Import Topics option. This will allow you to bring those topics into your current project seamlessly.

![Screenshot 2024-11-18 at 11.46.55.png](<../assets/images/Screenshot 2024-11-18 at 11.46.55.png>)


- **Other project** If you have previously worked with similar text data in Caplena, you can utilize any suitable project as a basis for your new project. This can help you leverage existing structures and settings to expedite your current analysis process. Even if the data is not 100% the same, but you expect a very similar structure and topics, this would be recommended.
- **File upload:** Here you can choose to import your topic collection directly into Caplena. This will help you to make use of existing topic collection created outside Caplena in the past. The file should be in Excel format and requires a certain structure, which you can see further below.


Following some more detail about each option.

### Other Project
By clicking on **"Other Project,"** you'll gain access to a list of projects you've previously created on the platform. Depending on your role, you will most likely also see the projects of other users of your organization. This means you can easily utilize the previous analyis of your team members and colleagues.

Once you've identified the appropriate project and the text column within it (procided it does have several text columns), simply click on the "Inherit Topic Collection" button located on the right side of the screen.

This action will enable you to seamlessly transfer the topic collection from the selected project to your current one, ensuring consistency and efficiency in your analysis process.

![Screenshot 2024-11-18 at 11.51.08.png](<../assets/images/Screenshot 2024-11-18 at 11.51.08.png>)



### Upload File
And finally, if you click on **upload file**, you will be able to bring your external topic collection) into the platform. Below you will find examples for the required format, depending on whether you will apply our topic sentiment or not.



Please change the format of your external topic collection into the format shown below before importing it.

 **Topic collection without sentiment:**

 ![Screenshot 2024-03-28 at 13.28.11.png](<../assets/images/Screenshot 2024-03-28 at 13.28.11.png>)

 **Topic collection with sentiment:**

 ![Screenshot 2024-04-10 at 10.45.07.png](<../assets/images/Screenshot 2024-04-10 at 10.45.07.png>)

By choosing the most suitable option based on your needs, you can optimize your workflow and enhance the efficiency of your analysis in Caplena.


## Topic Sentiment

When the system asks if your project contains sentiment, it’s important to understand what this means for your analysis.

Sentiment refers to whether responses in your project are positive, negative, or neutral. This is often used in projects like NPS  studies or any other survey where feedback can range from positive to negative.

- If your project involves responses that can express emotions, opinions, or feedback (such as customer or employee surveys where people might express satisfaction or dissatisfaction), you should select "Yes." 

- If the responses are purely factual (such as improvement questions) and don’t express positive or negative feelings, you should select "No."

If you´re not familiar with your data, click "View Rows" on the right side of the sentiment screen to preview your responses. 

![Screenshot 2024-10-29 at 12.08.59.png](<../assets/images/Screenshot 2024-10-29 at 12.08.59.png>)



## Topic Generation

After the AI generates the initial analysis structure for your project, you'll be taken to a screen where you can review and refine it.

![Screenshot 2024-10-29 at 12.12.53.png](<../assets/images/Screenshot 2024-10-29 at 12.12.53.png>)


 This structure is organized into two levels: categories and topics. Here’s what to do next:

**Step 1: Review Categories**

- **Rename:** If a category name doesn’t quite fit, feel free to rename it to something more suitable.
- **Remove:** If a category doesn’t apply to your data, you can remove it entirely.
- **Add:** If you think of another important category that the AI didn’t include, go ahead and add it manually.

**Step 2: Check Topics**

- **Apply the MECE Principle:** Ensure that topics are Mutually Exclusive, Collectively Exhaustive (MECE):
1. **Mutually Exclusive:** Topics should not overlap. Each topic should represent a unique idea or theme.
2. **Collectively Exhaustive:** Together, all topics should cover all possible aspects of the category, leaving no gaps

- **Use AI Suggestions:** Look at the AI-generated suggestions on the right to remove potentially similar topics.

![Screenshot 2024-10-29 at 12.14.47.png](<../assets/images/Screenshot 2024-10-29 at 12.14.47.png>)


 **Step 3: Finalize and Refine**

- **Make final adjustments** to the structure if needed
 - **Generate More Topics:** Click "Generate More Topics" to add more topics for specific categories or the entire project.

![Screenshot 2024-10-29 at 12.16.02.png](<../assets/images/Screenshot 2024-10-29 at 12.16.02.png>)


 <!-- theme: info -->

> During each of the three stages, you'll see the Row Browser on the right-hand side. This tool is useful if you want to review the actual data in your project as you refine the structure.

![Screenshot 2024-10-29 at 12.16.51.png](<../assets/images/Screenshot 2024-10-29 at 12.16.51.png>)






