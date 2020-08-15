# ICE \(Individual Conditional Plots\)

### Introduction

ICE is short for Individual Conditional Expectation. These plots are similar to the PDPs, yet very different.

They are similar to PDPs because they help in understanding the variations in a feature values against the output. In essence, they are extension to the PDPs. An ICE plot can be aggregated to get a PDP plot. The ICE plot unpacks the PDP curve and displays one line per instance that shows how the instance prediction changes when feature changes.

‌They are different than PDPs because they help achieve local interpretability, rather than the global interpretation we get from PDPs. 

### **Non Technical Explanation:**

To explain the ICE concept, we will take the same example to the one in PDPs to help draw the analogy between the PDP and ICE as well.

In PDPs, we said that a feature refers to a subject - Physics, Chemistry or Math. In PDP analogy, we mentioned that to study how an individual subject impacts the overall student performance, the teacher took PDP approach. 

![](../.gitbook/assets/image%20%2865%29.png)

Suppose the teacher was not satisfied with the results in PDP and decided to dive deeper with the ICE approach. In ICE, we do not average the scores for the other subjects. Rather, we plot the Math score variations with the actual Physics and Chemistry scores.

So in the ICE approach, the teacher gets multiple lines in the plot - one for every test. Each line shows how the overall performance varies with Math scores, but with the different Physics and Chemistry scores that the student had scored. This gives a more detailed insight to the teacher on how the student's tests have been going. 

The teacher observes that the first test line is well below the last test line. This signifies that the overall performance has gone up from the beginning of the year and that the student has improved in Math. 

This is the power of ICE plots. They allow one to study the individual rows of data in more detail.   

### Technical Explanation:

As stated before, ICE plots represent feature variations for every individual row. When the variations for every single row are in the same plot, we can see if there are any relations between individual rows or subsets of data.

In the below image, we can see the effect of a feature "Age" on the Cancer prediction probability. How do we interpret this plot? 

First, we see that majority of the lines correspond to low cancer prediction probability. So our data set has the majority of people with low predictions of getting cancer. 

Second, we see that there is an increase in the probability of getting cancer at the age of 50. This is a big interpretation and speaks volumes on the data we are studying. 



![](../.gitbook/assets/image%20%2837%29.png)

‌Due to a large amount of data instance, it will be difficult to understand the difference between the individual instances. But, we can find patterns in a group of instances. Above, we see that people with a low probability of cancer \(less than 0.2\) would continue to have a low probability as they grow. 

#### Centered ICE plots

‌Many times interpreting the individual lines may not be easy and can pose a problem. Centered ICE plots provide a simple solution by centering the curves at a certain point in the feature and displaying only the differences in prediction.

![](../.gitbook/assets/image%20%2836%29.png)

The C-ICE \(centered ICE plots\) makes it easier to compare the curves of individual instances. 

#### Derivate ICE plots

It helps to Identify the heterogeneity within the data. The derivate function \(curve\) will tell you whether changes occur and in which direction they occur. If there are no interactions then the individual partial derivate will be the same and they differ due to interaction which will be visible in derivate ICE -plot. So Derivate ICE plot can be used to identify the interaction among the features.

### Visualizations



![](../.gitbook/assets/image%20%28120%29.png)

![](../.gitbook/assets/image%20%28122%29.png)

**References**

1. Molnar, Christoph. "Interpretable machine learning. A Guide for Making Black Box Models Explainable", 2019. [https://christophm.github.io/interpretable-ml-book/](https://christophm.github.io/interpretable-ml-book/). \(the images were taken from here\)
2. [The Elements of Statistical Learning](https://web.stanford.edu/~hastie/ElemStatLearn/): Trevor Hastie,  Robert Tibshirani and  Jerome Friedman

