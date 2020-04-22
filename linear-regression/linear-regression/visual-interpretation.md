---
description: >-
  The information of the weight table (weight and variance estimates) can be
  visualized in a weight plot.
---

# Visual Interpretation

The following plot shows the results from the previous linear regression model.  


![](../../.gitbook/assets/weightplot.PNG)

Notice that in the above weight plot, all weights are between 0 and 1. This is because the data has been standardized before fitting the model. The weight plot shows that being a smoker has a strong positive effect on the charges. Other features that have reasonable positive effect are the BMI and Age of an individual. Now that we have interpreted the coefficients, let us interpret the t statistic.   


A definition that can be found on Princeton University website\([link](https://dss.princeton.edu/online_help/analysis/interpreting_regression.htm)\)is:

The t statistic is the coefficient divided by its standard error. The standard error is an estimate of the standard deviation of the coefficient, the amount it varies across cases. It can be thought of as a measure of the precision with which the regression coefficient is measured. 

Ok, but how do we use this statistic to interpret our model? Well, we can simply remember that any value greater than 2 or lesser than -2 in the t statistic implies that the particular feature is important. If you want to know why these values in particular were chosen, have a look at this [article](https://blog.minitab.com/blog/adventures-in-statistics-2/understanding-t-tests-t-values-and-t-distributions).

So in our model, all the features have a t-value greater than 2 or lesser than -2 except the feature “sex”. The t value for this feature is 0.394. Which implies this feature is insignificant. So the medical charges are not too gender biased as per our dataset. The fact that this feature is not very significant is the reason it is missing from our weight plot above.   


