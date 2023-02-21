---
stoplight-id: 9aad852f0ab9a
---

# Correlation Metrics

In our Relationship chart, we offer different metrics which measure the correlation between topics. The conceptually simplest measure is the co-occurrence but the other metrics we offer are more indicative and less dependent on the topic distribution.

## 1. Co-occurrences
Co-occurrence enable you to discover and group concepts that are strongly related within the set of documents or records
More concretly, it is the number of time the topics appear together. This does not take into account the overall frequency of the topic and is thus biased on frequent topics.

## 2. Jaccard Index

The Jaccard value is a measure of similarity between two topics, with a range between 0 and 1.0. A high value indicates a high similarity.
It is computed by dividing the intersection of the co-occurrences toics by their union.
This measure is more robust towards the topic distribution than co-occurrence.

### **Example :**

Imagine we have only two topics : Design, and Product.
Design and Product are mentioned together 12 times, and are mentioned in total 20 times (either together or independently of each other).

The Jaccard index would then be : 12/20 = **0.6**


## 3. Kulczinsky measure (recommended)

The Kulczinsky measure ranges from 0 to 1 and indicates the average conditional probability of co-occurrences. A higher value indicates a higher similarity. This is the measure that deals most effectively with imbalance in the topic distribution.

The Formula is the following:

  0.5 * (A/(A+B)+ A/(A+C))


 with
 
- A = co-occurrence of both topics.
- B = number of times only the topic 1 is assigned. 
- C = number of times only the topic 2 is assigned.  

### **Example :**

We want to calculate the Kulczinsky value between Design and Product. 

- Design and Product have been mentioned together 55 time, so **A =100**
- Design has been mentioned 20 times (without Product), so **B = 20**
- Product has been mentioned 80 times (without Design), so  **C = 80**

The Kulczinsky value would be calculated the following way :

0.5 * ( 100/120 + 100/180) = 0.7