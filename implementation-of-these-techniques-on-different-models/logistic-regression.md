# Logistic Regression

Logistic regression is one of the techniques of machine learning from the field of statistics. The logistic regression model gives the probabilities of the K classes via linear functions while at the same, sum to one, and remains in \[0, 1\]. The name logistic regression comes from the use of the logistic function.  
****

To read more about Logistic Regression this [link](https://web.stanford.edu/~hastie/ElemStatLearn/).  


Logistic regression is applied to the Sales Opportunity Size Dataset where the **target** is   


**DEAL SIZE** - Small, Medium and Large  


The data is passed through preprocessing which contains handling missing values, one-hot encoding, and other steps required, then it is trained using Scikit learn Library.  


The model has very good accuracy, which can be seen in the confusion matrix which gives out very good output.  
****

**Image of the confusion matrix**  


Now since the model taring and predicting is done now time to move ahead with Interpretation, for this model we will be using SHAP for interpretation.  


We are using library SHAP by [Scott Lundberg](https://scottlundberg.com/) for generating SHAP for providing interpretation for the model trained.  
****

**Kernel Shap**

Kernel Shap is being used to generate SHAP values, kernel SHAP can be applied to any model for SHAP generation. Kernel SHAP uses a specially-weighted local linear regression to estimate SHAP values for any model.  
****

