# Assumptions

[Code Implementation here](https://colab.research.google.com/drive/1-TLYC_YdscL1CVMPJGxwEzY0tgw7BeqQ?usp=sharing)

### **Linearity** 

A linear regression model is used when the dependent variable y is assumed to vary linearly with dependent variables X \(X1, X2, X3,..., Xn\).

Fitting a linear model to non-linear data results in serious prediction errors. ‌ To detect non-linearity, one can inspect plots of 'predicted values' vs 'observed values'.

The desired outcome is that the points that are symmetrically distributed around a diagonal line in the plot \(such as that shown below\).

![](../../.gitbook/assets/image%20%28108%29.png)

### **Homoscedasticity**

Homoscedasticity means that the variance around our linear regression line is the same for all the values of predictor variables. In other words, Homoscedasticity describes a situation in which the error term is the same across all the values of the independent variables/feature inputs. Violation of the Homoscedasticity is called Heteroscedasticity. Heteroscedasticity is present when the size of the error term is different across different values of an independent variable. This can be fixed by data transformation methods such as log transformation.

![](../../.gitbook/assets/image%20%28105%29.png)

![](../../.gitbook/assets/image%20%28104%29.png)

### **No Multicollinearity** 

Multi-collinearity is a situation wherein the independent variables in the regression model are highly correlated. Multi-collinearity is not good for linear modeling.

One can detect Multi-collinearity by using the Variance Inflation Factor\(V.I.F.\). The Variance Inflation Factor estimates how much the variance of a regression coefficient is inflated due to Multi-collinearity in the model.

**V.I.F.** = 1/\(1-Rsquare\) \(photos needed\)

Variance Inflation Factors range between 1 and above 1. The numerical value for V.I.F. tells us what percentage of the variance \(i.e. the standard error squared\) is inflated for each coefficient. 

Let's take an example to understand this concept better:

Assume V.I.F. = 1.9 

This tells us that the variance of a particular coefficient is 90% bigger than what you would expect if there was no Multi-collinearity — if there was no correlation with other predictors. 

General Values for Variance Inflation Factor:

**1** = not correlated

**Between 1 and 5** = moderately correlated

**Greater than 5** = highly correlated

### **Normality test**

When we apply a linear model, we essentially do hypothesis testing. The test the hypothesis that a particular feature input has an impact on the target variable. In order to apply hypothesis testing, the data has to be normally distributed. This is required while making the linear model also. The normality can be verified with a normal quantile-quantile plot. If the plot is an approximately straight line, then the data is approximately normally distributed.

Violations of normality may occur because:  

* the dependent and/or independent variables are significantly non-normal
* the linearity assumption is violated

The solution can be a nonlinear transformation of variables that might help to make data normal.

![](../../.gitbook/assets/image%20%2812%29.png)



