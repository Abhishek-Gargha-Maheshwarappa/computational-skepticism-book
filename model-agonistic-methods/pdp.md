# PDP \(Partial Dependence Plot\)

**Readers note:** _**The book is not yet completed will be released in the last week of August**_

### Introduction

Partial Dependence Plots were first used by Friedman in 2001. The model agnostic technique plots the change in a specified feature's values with the predicted outcome, averaging the effect of the other predictor variables. By making such a plot, we can get a gist of how a feature impact varies  - linear, non-linear,  etc. 

These plots were one of the earliest techniques used to interpret machine learning models. Essentially, the plot shows the marginal effect of a feature on the predicted outcome of a machine learning model. The plots help get an insight into the feature importance. A simple way to judge feature importance from these plots is \(a\) if the plot is zero or a constant line, then the feature is not very important in predicting the outcome \(b\) if the plot has a linear or has many curves, then the feature is important as it is impacting the predictor outcome.

### Mathematical Explanation

It is often used to study the relationship between the target and a feature under investigation. 

Input predictor variables XT = \(X1, X2, . . . , Xp\) - indexed by S ⊂ {1, 2, . . . , p}.

Consider the subvector XS of ℓ &lt; p of the predictor variable

Let C be the complement set,  -  S ∪ C = {1, 2, . . . , p}

A general function f\(X\) will in principle depend on all of the input variables

 f\(X\) = f\(XS , XC\)

One way to define the average or partial dependence of f\(X\) on XS is

![](../.gitbook/assets/image%20%2833%29.png)

PDP can be Estimated by

![](../.gitbook/assets/image%20%2832%29.png)

where {x1C, x2C, . . . , xNC} - values of XC occurring in the training data. 

### **Non-Technical Explanation**

The way PDPs work is very similar to how one would 

### **Technical Explanation** 

To understand how PDPs work, let us take the example of medical insurance charges and the data set for this problem that we have mentioned in the Datasets section.

In this, the insurance charges are modeled on: -

* Age
* BMI
* Sex
* Smoker
* Region

Now we know that insurance charges depend on all the above features. What if I want to know how age affects the premium? or how does smoking affect my insurance charge? Its intresting to understand these things right, so that company can make a proper risk assessment and customers can understand how to manage these things to handle charges. Age cannot be managed but smoking can be stopped if it is increasing the premium probably the right reason to quit smoking.

That's where you average out the other features other than the one of feature which of interest, and observe how the output varies. This can be visually represented by a partial dependence plot.

Here if we take a partial dependence plot for prediction versus age, then the partial dependence plot tells how prediction varies with respect to age averaging out all other features. 

### Visualizations

![](../.gitbook/assets/image%20%2829%29.png)

Image credits - [https://scikit-learn.org/](https://scikit-learn.org/)

### Pros

PDP is very intuitive 

PDP has causal interpretation has it averages the other features



### Cons

PDP requires a pass over the entire dataset once, which can be computationally intensive, even for moderately sized data sets. 

‌It can be applied with a maximum of two features due to the higher dimensional view is not possible to plot and understandable due limitation of the human perception. It is generally applied to the most important features and can have multiple PDPs side by side. 

### Reference 

The Elements of Statistical Learning: [Trevor Hastie](http://www-stat.stanford.edu/~hastie/),  [Robert Tibshirani](http://www-stat.stanford.edu/~tibs/) and  [Jerome Friedman](http://www-stat.stanford.edu/~jhf)

Scikit Learn -  [https://scikit-learn.org/](https://scikit-learn.org/)



