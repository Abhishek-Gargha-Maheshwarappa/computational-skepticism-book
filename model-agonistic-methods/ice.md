# ICE \(Individual Conditional Plots\)

**Readers note:** _**The book is not yet completed will be released in the last week of August**_

ICE display one line per instance that shows how the instance prediction changes when feature changes.

‌ PDP focus is on the global interpretation and doesn't concentrate on local interpretation. ICE is equivalent to PDP for individual data instance, PDP is the average of ICE lines

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

