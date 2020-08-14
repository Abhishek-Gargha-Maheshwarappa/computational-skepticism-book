# Linear Regression

**Readers note:** _**The book is not yet completed will be released in the last week of August**_

A linear model is an attempt to understand the target variable as a linear equation of the features_. **In other words, a linear model predicts the dependent variable as a weighted sum of the independent variables. The linearity of the established relationship makes the interpretation easy.**_ Linear regression models are very widely used by statisticians, computer scientists and other people who tackle quantitative problems. It is safe to say that almost every machine learning engineer started his/her journey with a simple linear regression model. 

The reason one uses a linear model because it is easy to implement and easy to understand. Every machine learning model is always made with a trade-off between interpret-ability and accuracy. Complex Deep learning models are highly accurate, but their structure makes it difficult to be interpreted. Linear models, on the other hand, can make reasonably accurate predictions and are easy to interpret.

 The only major drawback of a linear model is that it does not replicate an ideal real-time scenario. The assumption that all relationships to a target variable are linear and that changing a feature input does not affect the other inputs makes one skeptical to use linear models. That being said, they are one of the oldest and traditional methods of making predictions with high interpret-ability. 

The learned relationships  in a linear model can be written for a single row/instance as follows:

y = β0 + β1 \*X1 + β2 \*X2 + β3 \*X3 .. + βn \*Xn + ϵ

Where :

* ϵ -  mean-zero random error term
* y - Dependent variable 
* X1, X2, X3,..., Xn - Independent variables
* β0 - Expected value of y when all X = 0 A.K.A Intercept
* β1, β2, β3,...,β4- Average increase in y associated with a one-unit increase in X A.K.A Slope

The equation format makes it very easy to understand how our prediction varies with change in every single feature input. In the coming sections, we will dive deeper into the assumptions of this model, the implementation & interpretation. Links to the Python notebooks are attached towards the end of every section for users.

