---
stoplight-id: 9jt98mwlpcfy9
---

# Chart Values Explained

**Why the sum of all topics within a category can be higher than the count of that category?**

All chart values and percentages are counted and calculated on a respondent level.

The value for an individual bar in a bar chart or a tile in the treemap represent the number of respondents for that category or topic. However, in some cases the sum of all topics within a particular category can be higher than the absolute number shown for the overall category. The reason for that is rather simple.

 - A category tends to contain different topics.
 - The individual answer from a respondent can cover several topics, thus, it is not unlikely that several topics will be assigned to an individual response.
 - In case that two topics from one category are assigned to one individual response, there is one count for that respondent for each of these two codes. However, to calculate the occurrence of the category as a whole, we do not want to count the individual respondent twice - even though the respondent gave two codes within that category, i.e. two "different flavors" of the overall category, the respondent should occur only once in the overall category count.

Lets have a look at an example to further illustrate the above. 

![Bildschirmfoto 2022-02-09 um 15.28.00.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/wiqekGcZlbw)

The chart above has two categories highlighted, which are `NETWORK` and `COMMUNICATION`. The category `COMMUNICATION` contains two topics, which are `Good / clear communication` and `Too much spam / advertising calls`. Both topics are mentioned twice and the value for the over category is four, which means we have four respondents for that category, two for each of the two codes.

When we are looking at the the category `NETWORK`, the situation is slightly different. There are two topics within the category (`Best network / good network` and `Connection good`), which add up to 20. However, the overall value for the category is only 19. In this case we have 19 respondents for that category, but the open ended answer from one of these respondent was assigned to both of the individual topics of that categories - which you can see in the example below.

![Bildschirmfoto 2022-02-09 um 15.06.06.png](https://stoplight.io/api/v1/projects/cHJqOjEyNDcxMw/images/DS7FovGzYi0)

<!-- theme: info -->
> In summary, **we always focus on the respondent level**, but this may lead to a slight discrepancy when comparing the overall value of a category and the sum of all topics within it.



