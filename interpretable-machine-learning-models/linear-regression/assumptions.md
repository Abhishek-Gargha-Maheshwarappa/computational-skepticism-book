---
description: What assumptions to be made?
---

# Assumptions

### **Linearity** 

The linear regression model is used when the dependent variable y is assumed to vary linearly with dependent variable X.

Fitting a linear model to non-linear data results is serious prediction errors. ‌ To detect non-linearity one can inspect plots of predicted values vs observed values.

The desired outcome is that points are symmetrically distributed around a diagonal line in the plot.

![](../../.gitbook/assets/image%20%2813%29.png)

### **Homoscedasticity**

Homoscedasticity means the variance around the regression line is the same for all the values of predictor variables. Homoscedasticity describes a situation in which the error term is the same across all the values of the independent variables. Violation of the Homoscedasticity is called heteroscedasticity, it is present when the size of the error term difference across values of an independent variable.

![](../../.gitbook/assets/image%20%2814%29.png)

![](../../.gitbook/assets/image%20%2812%29.png)

### **No Multicollinearity** 

Multicollinearity is the situation where independent variables in the multiple regression model are highly correlated. Multi collinearity is not good for linear modeling.

One can detect multicollinearity using the Variance Inflation Factor\(VIF\). The Variance Inflation Factor estimates how much the variance of a regression coefficient is inflated due to multicollinearity in the model.

**VIF** = 1/\(1-Rsquare\)

#### **Interpreting the Variance Inflation Factor**

Variance Inflation Factors range from 1 upwards. The numerical value for VIF tells us what percentage of the variance \(i.e. the standard error squared\) is inflated for each coefficient. 

Let take an example,

VIF = 1.9 

tells us that the variance of a particular coefficient is 90% bigger than what you would expect if there was no multicollinearity — if there was no correlation with other predictors. 

**Variance Inflation Factor:**

**1** = not correlated

**Between 1 and 5** = moderately correlated

**Greater than 5** = highly correlated





1. **Linearity**: The relationship between X and the mean of Y is linear.
2. **Homoscedasticity**: The variance of residual is the same for any value of X.
3. **Independence**: Observations are independent of each other.
4. **Normality**: For any fixed value of X, Y is normally distributed.





[The Notebook with the implementation of the Assumptions](https://colab.research.google.com/drive/1-TLYC_YdscL1CVMPJGxwEzY0tgw7BeqQ?usp=sharing)









