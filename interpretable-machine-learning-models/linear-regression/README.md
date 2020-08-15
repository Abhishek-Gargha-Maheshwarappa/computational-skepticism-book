# Linear Regression

A linear model is an attempt to understand the target variable as a linear equation of the features. In other words, a linear model predicts the target\(dependent\) variable as a weighted sum of the independent variables. The linearity of the established relationship makes the interpretation easy. Linear regression models are very widely used by statisticians, computer scientists and other people who tackle quantitative problems. It is safe to say that almost every machine learning engineer started his/her journey with a simple linear regression model. 

![](../../.gitbook/assets/image%20%2892%29.png)

An example of Linear Regression in daily life occurs when a person is looking for an apartment. After looking at a few apartments, we get to know the price and other information like size of the house, number of rooms, number of bathrooms, etc. With this information, the person builds a linear model in their mind that will approximate the apartment cost for any apartment based on the details of rooms, size, bathrooms, and others.

The reason one uses a linear model because it is easy to implement and easy to understand. Every machine learning model is always made with a trade-off between interpret-ability and accuracy. Complex Deep learning models are highly accurate, but their structure makes it difficult to be interpreted. Linear models, on the other hand, can make reasonably accurate predictions and are easy to interpret.

 The only major drawback of a linear model is that it does not replicate an ideal real-time scenario. The assumption that all relationships to a target variable are linear and that changing a feature input does not affect the other inputs makes one skeptical to use linear models. That being said, they are one of the oldest and traditional methods of making predictions with high interpret-ability. 

The learned relationships  in a linear model can be written for a single row/instance as follows:

![](../../.gitbook/assets/image%20%2894%29.png)

The equation format makes it very easy to understand how our prediction varies with change in every single feature input. In the coming sections, we will dive deeper into the assumptions of this model, the implementation & interpretation. Links to the Python notebooks are attached towards the end of every section for users.

