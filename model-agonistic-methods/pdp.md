# PDP \(Partial Dependence Plot\)

**Readers note:** _**The book is not yet completed will be released in the last week of August**_

### Introduction

Partial Dependence Plots were first used by Friedman in 2001. This model agnostic technique plots the variations in a specified feature's values with the change in predicted outcome, averaging the effect of the other predictor variables. By making such a plot, we can get a gist of how a feature impact varies  - linear, non-linear,  etc. 

These plots were one of the earliest techniques used to interpret machine learning models. Essentially, the plot shows the marginal effect of a feature on the predicted outcome for a machine learning model. As a result, the plots help get an insight into the feature importance. A simple way to judge feature importance from these plots is \(a\) if the plot is zero or a constant line, then the feature is not very important in predicting the outcome \(b\) if the plot has a linear slope or has many curves, then the feature is important as it is impacting the predictor outcome.

### **Non-Technical Explanation**

The way PDPs work is very similar to how a teacher would evaluate students in a classroom. Consider the example wherein a Math teacher has been assigned a new group of students to teach. In order to understand the students better, the teacher want to know how the students fair currently. 

In order to do this, the teacher gives the students a test to see their performance. The test results arrive a week later and the teacher starts to evaluate the students. Only once all the students marks have been evaluated, the teacher can start evaluating how an individual student fairs in the class. 

![](../.gitbook/assets/image%20%2839%29.png)

Once the teacher has all the marks evaluated, in order to find out the students that are highly skilled in math, the teacher will average out the marks by all students and compare individual student marks to that average. The more a student is above the average, the better he/she is at math. 

![](../.gitbook/assets/image%20%2838%29.png)

PDPs are similar to the above evaluation such that the students are merely the features present in the data set. To study the impact of one feature, we average the effect of the others and study that particular features values with change in prediction outcome.

### **Technical Explanation** 

A common misconception in PDPs is that we want to plot the feature values against the predicted outcome. NO! We want to plot the feature values against the change in our predicted outcome. So the feature values are the x-axis and the change in prediction values for every feature value input is the y-axis.

For features that are continuous, it is easy to visualize a line that shows the variations in a particular column. For categorical columns, the plots are not exactly a straight line, rather discrete. The PDP takes the form of a bar plot and all the categories present in the column under investigation have unique bars assigned to them.

![](../.gitbook/assets/image%20%2840%29.png)

If the bars are similar in size and value range, then the feature is not very important and does not change the prediction much. Else, if the bar size and value ranges are different, the feature is important and the plot gives an idea of the most impactful categories in the column.

The reason PDPs work well is because the help establish a relationship between a column and the output.

We know that the output depends on input features but to what if we only want to study one particular feature relation with the output? It is interesting to understand these things because if a column is highly impacting or changing the output, we want to be able to control that change as much as possible.

Note: PDPs can also be used to visualize the effect of two columns together against the change in output, in the form of a 3-D plot. \(see visualizations below\)

### Visualizations

![](../.gitbook/assets/image%20%2841%29.png)

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



