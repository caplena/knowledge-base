---
stoplight-id: vq49kyqjngzva
---

### Driver Analysis

Key driver analysis is a powerful way of measuring the relative impact of topics on a KPI. The following explains in detail how we utilize this in Caplena combining the categorization of the open ended text comments together with ratings and performance measures.

The driver analysis is aiming to help you to **understand the impact of a topic mentioned on a performance metric**, such as the likelihood to recommend, overall satisfaction, star rating, etc.

The driver analysis includes four key elements 👇

| Chart Section                   | Details                |
| ------------------------------- | ---------------------- |
| **Impact per row**                  | Measuring the impact on the performance metric on an individual basis. <br> Based on a multiple regression analysis.     |
| **Net impact**                      | Showing the current impact on the performance metric. <br> Based on the driver strength (impact per row) and the frequency of the topic mentioned.     |
| **Suggestions for improvement**     | AI-generated suggestions and recommendations on how to improve key topics, helping you to take the right actions to boost satisfaction.   |
| **Driver Impact vs. Mentions**                          | A scatter plot to visualize strength & weaknesses by visually combining driver strength and frequency. <br> *See second screenshot, the visualization can be switched on.*|

The following screenshot shows an example with the likelihood to recommend (NPS) as dependent variable.

![Bildschirmfoto 2025-04-16 um 16.50.22.png](<../assets/images/Bildschirmfoto 2025-04-16 um 16.50.22.png>)


Let’s have a look at the example above and interpret some of the results.

##### Impact per row
**Topic sentiment** plays a key role for the driver analysis, allowing us to **determine the impact of a topic mentioned based on positive and negative experiences**. The color coding of the bars reflects the impact taking sentiment into account. The numbers next to the bars show regression coefficients. The higher (or lower) the number, the stronger the suggested impact on the likelihood to recommend.

The impact or the driver strength can be very different for each individual topic.
* Taking `NETWORK QUALITY / Reliability` as an example. The red and green bar are of nearly equal length which means a positive as well as a negative experience will drive the likelihood to recommend notably to either side of the scale, i.e., someone mentioning an unreliable network quality would most likely not recommend the network provider in question.
* Taking `DEALS & PRICING / Price` as another example. A negative price perception has a very strong negative impact on the likelihood to recommend. At the same time, a positive perception does not impact / drive the likelihood to recommend very much. On this topic, one can only avoid punishment, but there is not much to gain on the positive side. Following the Kano model, this could indicate a so called “hygiene driver”, meaning that customers expect attractive prices, but react strongly when perceived otherwise.

##### Net impact
The impact per row is an interpretation on a case basis. Any given topic might be a very strong driver with a very high impact on a customer’s likelihood to recommend, but **to measure the overall impact on a KPI over the total sample we need to consider the frequency** in which that topic was mentioned.

For the net impact calculation we **multiply the driver strength with the frequency of a topic mentioned** allowing us to determine to what extend the NPS (in our example) is influenced overall.

The impact shown for each row reflects the case-specific interpretation. While a particular topic might be a strong driver of a customer’s likelihood to recommend—indicating high individual impact—it’s important to also consider how frequently that topic is mentioned across the entire sample to understand its overall influence on a KPI.
To calculate net impact, we multiply the driver strength by the frequency of the topic. This gives us a clearer picture of the topic’s total contribution to the KPI (such as NPS) across the full dataset.
Taking `BRAND PERCEPTION / Overall perception` as an example. This topic has the highest net impact based on the combination of driver strength and frequency.
-	Even though the negative impact of that topic is very high, when happening for individual customers, in most cases the experience is positive, which is the cause of the strong net contribution.
-	The topic is mentioned often (n = 191, see under mentions in the screenshot), but other topics are mentioned at a higher frequency. However, driver strength and the number of positive mentions of the topic eventually determine the net impact.
The net impact shows the current impact or current contribution to a score or rating. In the case of the NPS and the above example, the net impact of `BRAND PERCEPTION / Overall perception` is 9.1, which means that this topic contributes 9.1 points to the NPS, whereas 3.8 are lost by the negative impact of `DEALS & PRICING / Price`.

>Note that now the driver chart supports NPS and 5 Star Rating as dependent variable. Other performance metrics will be added shortly.

###### Suggestions for improvement
For each topic we show AI-generated suggestions based on the open text data as well as the driver calculations. In the example above, the three suggestions take up several aspects of the chosen topic `NETWORK QUALITY / Connectivity & coverage`, but also takes and angle beyond the topic when relations are being discovered such as the pricing.

###### Driver Impact vs. Mentions
A click on the icon at the top left of this section will switch from the suggestion to the scatter plot showing the relative impact of a topic by the extension to the right (positive impact) and to the left (negative impact). The vertical axis gives an indication of the frequency.

![Bildschirmfoto 2025-04-16 um 16.55.49.png](<../assets/images/Bildschirmfoto 2025-04-16 um 16.55.49.png>)

Check out the video guide below for a quick walkthrough:

https://www.youtube.com/watch?v=eqvRyJ8EiHY
