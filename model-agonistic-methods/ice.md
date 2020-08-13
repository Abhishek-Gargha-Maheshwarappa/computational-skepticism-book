# ICE \(Individual Conditional Plots\)

**Readers note:** _**The book is not yet completed will be released in the last week of August**_



### Introduction

ICE is short for Individual Conditional Expectation. These plots are similar to the PDPs, yet very different.

They are similar to PDPs because they help in understanding the variations in a feature values against the output. In essence, they are extension to the PDPs. An ICE plot is just the PDP but disintegrated for every instance in the data set. The ICE plot unpacks the PDP curve and displays one line per instance that shows how the instance prediction changes when feature changes.

‌They are different than PDPs because they help achieve local interpretability, rather than the global interpretation we get from PDPs. 

### **Non Technical Explanation:**

To explain the ICE concept, we will take the same example to the one in PDPs to help draw the analogy between the PDP and ICE as well.

In PDPs, we said that a feature refers to a student. There were 10 students and 20 tests in our example . In PDP analogy, we mentioned that to study if John helped improve class performance, the teacher took PDP approach. 

Suppose the teacher  In ICE, we want to be able to visualize how the student scored in reality. For every test, we plot how the student scored in Math with the actual Physics and Chemistry scores.  





### Technical Explanation:

As stated before, ICE plots represent feature variations for every individual row. When the variations for every single row are in the same plot, we can see if there are any relations between individual rows or subsets of data.

Technically, the plots are similar to PDPs as the effect of other features are averaged out. 



![](../.gitbook/assets/image%20%2837%29.png)

‌ Due to a large amount of data instance, it will be difficult to understand the difference between the instance.

‌ So how to decode it, how to get around it .....!!!!

#### Centered ICE plots

‌ Here come centered ICE plots to the rescue, a simple solution is to center the curves at a certain point in the feature and display only the difference in prediction.

![](../.gitbook/assets/image%20%2836%29.png)

The C-ICE \(centered ICE plots\) makes it easier to compare the curves of individual instances.

#### Derivate ICE plots

It helps to Identify the heterogeneity within the data. The derivate function \(curve\) will tell you whether changes occur and in which direction they occur. If there are no interactions then the individual partial derivate will be the same and they differ due to interaction which will be visible in derivate ICE -plot. SO Derivate ICE plot can be used to identify the interaction among the features.

### References

1. Molnar, Christoph. "Interpretable machine learning. A Guide for Making Black Box Models Explainable", 2019.
2. The Elements of    Statistical Learning:   Trevor Hastie   , Robert Tibshirani   , Jerome Friedman

