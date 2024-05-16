---
stoplight-id: 1mvwn66uzqb9q
---

# Using Additional Columns as Segments

Any additional variable can be used to slice and dice your data based on specific criteria, such as demographics, location, or other relevant factors. Additional variables can be found under any “Add Filter” button under “Additional Columns”, when looking at:

- **Topic Assignment**
- **Charts**
- **Dashboards**

<!-- theme: info -->
>Example Scenario:
>Suppose you want to analyze customer feedback by age, you can use the "Age" column as an additional variable to filter or segment and compare responses by different age brackets.

![Screenshot 2024-05-16 at 13.30.59.png](<../assets/images/Screenshot 2024-05-16 at 13.30.59.png>)



## Creating Charts with Segments

Charts can be created from the Cockpit of any of your projects or via the main menu (top left next to the Caplena logo under “Charts”). When entering the charting you are in the Chart Setup, where you can choose the chart type on the top left. To compare segments in a single chart select the Bar Chart.

To compare segments in a bar chart you have two options.

- **Option 1:** Use the “auto-segmentation” for a one click comparison by additional column.
- **Option 2:** Create individual segments tailored to your needs. As the auto-segmentation is limited to a maximum of 15 different values for categorical variables, this is your choice in case you want to compare segments from an additional column which includes more than 15 attributes. Such columns would not being displayed as a choice in the auto-segmentation.

### Option 1: Auto-Segmentation

When you select the bar chart from the chart library on the left, you will see the “Segment By” menu at the bottom left. Here you can click on any of the options and created segmented charts by
- **Sentiment** to break the results by positive, negative, and neutral.
- **Numerical columns** where all your numerical columns will be available to choose from. The system will create the number of segments selected. No worries, the segments can be adapted, please see below how to do it.
- **Categorical column** for a break for any column with labeled attributes.
- **NPS column** to break the data by the three NPS groups (Promoters, Passives, and Detractors), just make sure the column with the likelihood to recommend was selected.

![Screenshot (30).png](<../assets/images/Screenshot (30).png>)

<!-- theme: info -->
>Segments can be edited!
>To edit a segment, click at the little arrow next to “Chart Setup” at the top left, which will bring you to the “Chart Settings”. At the bottom left you will see your segments.

![Screenshot (31).png](<../assets/images/Screenshot (31).png>)

To make any change to any of these segments you can click on the edit symbol at the right to the segment's name.
 Once in the segment, you can change the segment's name (as it will be shown in the legend) as well as the segment's properties, which in most cases will be one filter that you can open and amend your selection. 
 You can also click on “Add Filter” at the bottom right, to a segment built across various additional columns. Here you can also change the colors of your segments by “overwriting” the automatic selection.

![Screenshot (32).png](<../assets/images/Screenshot (32).png>)

### Option 2: Manual Creation of Segments

You can build the segments into a bar chart from scratch, the option to choose when your additional column exceeds the limit of 15 attribute value choices or when you want to use a column type going beyond the auto-segment choices, such as time period based on a date variable.

When you select the bar chart you click on the little arrow next to the “Chart Setup” at the top right and you will arrive at the “Chart Settings”. As you did not select a segmentation, you will see one segment which is the total segment across all data of the project.

![Screenshot (33).png](<../assets/images/Screenshot (33).png>)

Next to the name of the segment, which is per default the project name, you see an edit icon as well as a duplicate icon. When clicking on edit, you will be able to change segment name, color, as well as the filter options. With the latter you will create your segment. Just click on “Add Filter” at the bottom left and select the additional column you want to use to build your segment.

![Screenshot (34).png](<../assets/images/Screenshot (34).png>)

Once the filter is selected, you change the name of the segment. Let’s say you chose “Age” as an additional column and your first segment is the group between 18 and 25 years. You select the group within the filter and change the name to your liking. Once this first segment was created, you click on the duplicate icon next to edit on your first segment and a copy of the first segment will be made. Now you click on the edit icon of the copy, change name and filter and continue until all the segments are created.

![Screenshot (35).png](<../assets/images/Screenshot (35).png>)

In case the colors are not different, just click on Colors in the chart menu on the left and select “Segment” instead of Category or Topic.

![Screenshot (36).png](<../assets/images/Screenshot (36).png>) 


