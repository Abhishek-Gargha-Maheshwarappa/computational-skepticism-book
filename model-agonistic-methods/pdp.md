# PDP \(Partial Dependence Plot\)

**Readers note:** _**The book is not yet completed will be released in the last week of August**_

### Introduction

The partial dependence plot shows the marginal effect of one or two features on the predicted outcome of a machine learning model. A partial dependence plot can show the relationship between the target and the features under investigation. PDP is a global method that considers all the data instances, it gives the global relationship of a feature with the predicted outcome. 

### Technical Explanation

Let Xs be the set of target features, where the input predictor variable are 

X T = \(x1,x2,........xp\) indexed by S belongs to {1,2,3,....p}

 Let Xc be its complement of Xs

f\(x\) = f\(Xc,Xs\)

f\(x\) depends on all the input features

So now PDP

fs\(Xs\) = EXcf \(Xs,Xc\)

PDP can be used to interpret any black box models

### 

![](../.gitbook/assets/image%20%2831%29.png)



### **Non-technical Explanation** 

Let us take the example of insurance 

Where insurance charges are modeled on: -

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

Pros



Cons

This will be computationally intensive, even for moderately size data sets. The most important thing to remember is the partial dependence functions represent the effect on Xs on f\(x\) after accounting for the \(average\) effects of the other variable Xc on f\(x\). They are not the effect of Xs on f\(x\) ignoring the effect of Xc.

‌It can be applied with a maximum of two features due to the higher dimensional view is not possible to plot and understandable due limitation of the human perception. It is generally applied to the most important features and can have multiple PDPs side by side. 



