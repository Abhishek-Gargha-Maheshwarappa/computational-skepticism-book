# PDP \(Partial Dependence Plot\)

**Readers note:** _**The book is not yet completed will be released in the last week of August**_

### Introduction

Partial Dependence Plots were first used by Friedman in 2001. This model agnostic technique plots the variations in a specified feature's values with the change in predicted outcome, averaging the effect of the other predictor variables. By making such a plot, we can get a gist of how a feature impact varies  - linear, non-linear,  etc. 

These plots were one of the earliest techniques used to interpret machine learning models. Essentially, the plot shows the marginal effect of a feature on the predicted outcome for a machine learning model. As a result, the plots help get an insight into the feature importance. A simple way to judge feature importance from these plots is \(a\) if the plot is zero or a constant line, then the feature is not very important in predicting the outcome \(b\) if the plot has a linear slope or has many curves, then the feature is important as it is impacting the predictor outcome.

### **Non-Technical Explanation**

The way PDPs work is very similar to how a teacher would evaluate the classroom performance in a school. Consider the example wherein the teacher is assigned a class of 10 students. The teacher takes 20 tests for every student in an academic year.  

Every test is evaluated by the teacher. At the end of evaluation of all 20 tests in the year, the teacher studies the performance of the class. To her delight, the class performance had improved a lot in a span of 1 academic year. The teacher is very happy and wants to give chocolates to students that improved the most and helped improve class performance. To be able to see how well a particular student did, the teacher takes the PDP approach.  

![](../.gitbook/assets/image%20%2840%29.png)

First student is John. Since the class performance metric is dependent on all 10 students, the teacher takes the average scores for all other 9 students and sees how Johns scores affected it. She takes the individual scores of John along with the average scores of other 9 to compute the class performance in every test. If the plot is a straight line, it means that John has scored the same marks in all the tests. It also means that John did not have much hand in improving the class performance. If, on the contrary, John had scored low in his first few tests and scored high in the tests towards the end of the year, the teacher would see a linear line with increasing slope in the plot. This would tell the teacher that John had played a major role in improving class performance and definitely deserves a chocolate!

![](../.gitbook/assets/image%20%2838%29.png)

PDPs are similar to the above example such that the students are merely the features\(columns\) present in the data set. The test scores are the rows. To study the impact on of one feature, we average the effect of the others and only study how a single feature's values bring change in prediction outcome.

### **Technical Explanation** 

PDPs are named Partial Dependence Plots for a reason. The end goal is to find out the partial derivative of a single feature with respect to the output.

A common misconception in PDPs is that we want to plot the feature values against the predicted outcome. NO! We want to plot the feature values against the change in our predicted outcome. So the feature values are the x-axis and the change in prediction values for every feature value input is the y-axis.

For features that are continuous, it is easy to visualize a line that shows the variations in a particular column. For categorical columns, the plots are not exactly a straight line, rather discrete. The PDP takes the form of a bar plot and all the categories present in the column under investigation have unique bars assigned to them.

![](../.gitbook/assets/image%20%2841%29.png)

If the bars are similar in size and value range, then the feature is not very important and does not change the prediction much. Else, if the bar size and value ranges are different, the feature is important and the plot gives an idea of the most impactful categories in the column.

The reason PDPs work well is because the help establish a relationship between a column and the output.

We know that the output depends on input features but to what if we only want to study one particular feature relation with the output? It is interesting to understand these things because if a column is highly impacting or changing the output, we want to be able to control that change as much as possible.

Note: PDPs can also be used to visualize the effect of two columns together against the change in output, in the form of a 3-D plot. \(see visualizations below\)

### Visualizations

![](../.gitbook/assets/image%20%2844%29.png)

![](../.gitbook/assets/image%20%2829%29.png)

### Pros

* PDPs are very intuitive 
* PDPs have causal interpretation as it averages the other features

### Cons

* PDP requires a pass over the entire dataset once, which can be computationally intensive, even for moderately sized data sets. 

  ‌It can be applied with a maximum of two features due to the higher dimensional view is not possible to plot and understandable due limitation of the human perception. It is generally applied to the most important features and can have multiple PDPs side by side. 

### Reference 

The Elements of Statistical Learning: [Trevor Hastie](http://www-stat.stanford.edu/~hastie/),  [Robert Tibshirani](http://www-stat.stanford.edu/~tibs/) and  [Jerome Friedman](http://www-stat.stanford.edu/~jhf)

Scikit Learn -  [https://scikit-learn.org/](https://scikit-learn.org/)



