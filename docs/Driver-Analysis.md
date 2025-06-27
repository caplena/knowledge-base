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
The impact of each row is interpreted on a case-by-case basis. A given topic may be a strong driver with significant influence on customer satisfaction or likelihood to recommend. However,** to assess the overall impact on a KPI across the entire sample, we must also consider how frequently the topic is mentioned**.

To calculate net impact, **we combine the strength of the driver with the frequency of mentions**, enabling us to determine the extent to which the topic influences the KPI at a broader level.

To calculate the net impact on metrics like CSAT, star rating, or any other average-based KPI, we can multiply a topic’s driver strength by its frequency of mentions. However, this straightforward multiplication does not apply to NPS, as changes in NPS are governed by a non-linear step function—for example, shifting from a score of 2 to 6 does not affect the classification; the respondent remains a detractor.

To address this, we use more **advanced probabilistic modeling to estimate the true net impact on NPS**. This approach accounts for the discontinuities in the scoring system and helps eliminate the “randomness” introduced by the step function, resulting in a more accurate representation of impact.

This provides a clearer understanding of each topic’s overall contribution to the KPI across the entire dataset.

Let’s take `BRAND PERCEPTION / Overall perception` as an example. This topic has the highest net impact due to the combination of its strong driver strength and relatively high frequency of mentions.

- While the negative impact of this topic can be substantial at the individual level, the majority of mentions are positive. This positive skew is what drives its strong overall contribution.

- Although it appears frequently (n = 191, as shown under Mentions in the screenshot), several other topics are mentioned even more often. However, the net impact is ultimately driven by both the strength of the topic as a driver and the volume of positive mentions.

The net impact represents a topic’s current contribution to a score or rating. In the case of NPS, for instance, `BRAND PERCEPTION / Overall perception` contributes +9.1 points, while the negative impact of `DEALS & PRICING / Price results` in a -3.8 point loss.

>Note that now the driver chart supports NPS and 5 Star Rating as dependent variable. Other performance metrics will be added shortly.

###### Suggestions for improvement
For each topic we show AI-generated suggestions based on the open text data as well as the driver calculations. In the example above, the three suggestions take up several aspects of the chosen topic `NETWORK QUALITY / Connectivity & coverage`, but also takes and angle beyond the topic when relations are being discovered such as the pricing.

###### Driver Impact vs. Mentions
A click on the icon at the top left of this section will switch from the suggestion to the scatter plot showing the relative impact of a topic by the extension to the right (positive impact) and to the left (negative impact). The vertical axis gives an indication of the frequency.

![Bildschirmfoto 2025-04-16 um 16.55.49.png](<../assets/images/Bildschirmfoto 2025-04-16 um 16.55.49.png>)

Check out the video guide below for a quick walkthrough:

https://www.youtube.com/watch?v=eqvRyJ8EiHY
