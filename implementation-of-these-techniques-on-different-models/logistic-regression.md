# Logistic Regression

### What is Logistic Regression?

Logistic regression is one of the techniques of machine learning from the field of statistics. The logistic regression model gives the probabilities of the K classes via linear functions while at the same, sum to one, and remains in \[0, 1\]. The name logistic regression comes from the use of the logistic function.

To read more about Logistic Regression this [link](https://web.stanford.edu/~hastie/ElemStatLearn/).

Logistic regression is applied to the Sales Opportunity Size Dataset where the **target** is 

**DEAL SIZE** - Small, Medium and Large.

The data is passed through preprocessing which contains handling missing values, one-hot encoding, and other steps required, then it is trained using Scikit learn Library.

The model has very good accuracy, which can be seen in the confusion matrix which gives out very good output.

![ confusion matrix](../.gitbook/assets/image%20%2859%29.png)



Now since the model training and predicting is done now time to move ahead with Interpretation, for this model we will be using SHAP for interpretation.

We are using library SHAP by [Scott Lundberg](https://scottlundberg.com/) for generating SHAP for providing interpretation for the model trained.

**Kernel Shap**

Kernel Shap is being used to generate SHAP values, kernel SHAP can be applied to any model for SHAP generation. Kernel SHAP uses a specially-weighted local linear regression to estimate SHAP values for any model.

Once the SHAP values are generated we can generate the summary plot from these values which tells us the effect of each attribute on the predictions. The SHAP summary is always better compared to the variable importance because of the coalition effect involved in the SHAP.

![Summary Plot](../.gitbook/assets/image%20%2860%29.png)

From the above summary plot, it is clear that SALES has the highest impact on the output of the prediction and it is the most important attribute and MSRP is the least important attribute. These help companies decide what is affecting their target and help them make strategies easily.

![plot](../.gitbook/assets/image%20%2862%29.png)

The above picture gives more information compared above summary plot it shows the distribution and SHAP values can be negative which shows the negative impact of the particular values.  
****

