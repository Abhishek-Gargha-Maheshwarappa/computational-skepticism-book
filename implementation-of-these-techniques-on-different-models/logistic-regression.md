# Logistic Regression - SHAP

### What is Logistic Regression?

* Logistic Regression a machine learning algorithms from the field of statistics 
* A Logistic regression model gives the probabilities of the K classes via linear functions while at the same, sum to one, and remains in \[0, 1\]
* The name Logistic Regression comes from the use of a logistic function within the algorithm

To read more about Logistic Regression this [link](https://web.stanford.edu/~hastie/ElemStatLearn/).

### **Making the Model** 

**Data set:** Sales Opportunity Size ; **Target:** DEAL SIZE \(Small, Medium and Large\).

The data is passed through pre-processing stage which contains handling missing values, one-hot encoding, and other steps required. Then it is trained using by calling a function from Scikit-learn library.

**Accuracy:** 99.24% 

![ Confusion matrix](../.gitbook/assets/image%20%2859%29.png)

### **Implementation of Interpretability**

We are using the SHAP library created by [Scott Lundberg](https://scottlundberg.com/) for generating SHAP and providing interpretation for the model trained.

**Kernel Shap** is one of the SHAP explainers that can be used to generate SHAP values. Kernel SHAP can be applied to any model for SHAP generation. Kernel SHAP uses a specially-weighted local linear regression to estimate SHAP values for any model.

![](../.gitbook/assets/image%20%2877%29.png)

We have used kmeans on the entire data set before feeding it to the SHAP explainer to reduce computation time. Essentially we want to be able to get the predicted values for the data set by the model.

### **Visualization**

#### **Summary Plot**

* Can be plotted after generating SHAP values for the entire dataset
* Tells us the effect of each attribute on the predictions
* Better than a regular variable importance because of the coalition effect involved in the SHAP calculation

![Summary Plot](../.gitbook/assets/image%20%2860%29.png)

**Interpreting Summary Plot:** From the above summary plot, it is clear that SALES has the highest impact on the output of the prediction - Deal Size. It is the most important attribute and MSRP is the least important attribute. These help companies decide what is affecting their target and help them make strategies easily.

![plot](../.gitbook/assets/image%20%2862%29.png)

The above visualization gives more information compared a summary plot as it shows the distribution of the shap values. If SHAP values are negative then they have negative impact on the output.

**Force Plot:**

\*\*\*\*

