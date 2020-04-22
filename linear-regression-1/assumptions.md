---
description: >-
  Whether a model is the “right” model depends on whether the relationships in
  the data meet certain assumptions, which are:
---

# Assumptions



* **Linearity Assumption**: The prediction is assumed to be a linear combination of features, which is both its greatest strength and its greatest limitation. If you suspect feature interactions or a nonlinear association of a feature with the target value, you can add interaction terms or use regression splines.
* **Normality Assumption:** The target outcome, given the features, follows a normal distribution. If this assumption is violated, the estimated confidence intervals of the feature weights are invalid.
* **Homoscedasticity \(constant variance\)Assumption**: The variance of the error terms is assumed to be constant over the entire feature space. Suppose we are to predict the value of a house given the living area in square meters. You estimate a linear model that assumes that, regardless of the size of the house, the error around the predicted response has the same variance. This assumption is often violated in reality. In the house example, it is plausible that the variance of error terms around the predicted price is higher for larger houses, since prices are higher and there is more room for price fluctuations. Suppose the average error \(difference between predicted and actual price\) in your linear regression model is 50,000 Euros. If you assume homoscedasticity, you assume that the average error of 50,000 is the same for houses that cost 1 million and for houses that cost only 40,000. This is unreasonable because it would mean that we can expect negative house prices. Below graphs should help visualize this concept more
* **//insert graphs**
* **Independence   Assumption**: Each instance is independent of any other instance. If you perform repeated measurements, such as multiple blood tests per patient, the data points are not independent. For dependent data you need special linear regression models, such as mixed effect models or GEEs. If you use the “normal” linear regression model, you might draw wrong conclusions from the model.
* **Fixed features   Assumption:** The input features are considered “fixed”. Fixed means that they are treated as “given constants” and not as statistical variables. This implies that they are free of measurement errors. This is a rather unrealistic assumption. Without that assumption, however, you would have to fit very complex measurement error models that account for the measurement errors of your input features. And usually you do not want to do that.
* **Absence of multicollinearity  :** You do not want strongly correlated features, because this messes up the estimation of the weights. In a situation where two features are strongly correlated, it becomes problematic to estimate the weights because the feature effects are additive and it becomes indeterminable to which of the correlated features to attribute the effects.

 



  

