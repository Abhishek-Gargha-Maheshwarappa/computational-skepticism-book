# SHAP

SHAP is the acronym for SHapley Additive exPlanations, it is a game theory approach to interpret the machine learning model.

It is a method of dividing up the gains or costs among features according to the value of their individual contributions to the predictions of the machine learning model. SHAP can be used not only for interpretation but also for feature selection for training the machine learning model for better accuracy.

SHAP can be applied to tabular data and image data. SHAP is a model agnostic method, which means it can be applied to any model.  


The interpretation SHAP can do is 

**Force Plot**  
  

The above interpretation shows how each feature is pushing or contributing to moving the base value \(the average model output over the training dataset\) of the output. Features that push prediction higher are shown in red and the features pushing the value lower are in blue.

### **Partial Dependence Plot** 

![](https://lh5.googleusercontent.com/xpaILWMid_xyQ7viUNI8rD584-C1uvJMNsh0LTpREJh4VRtLHYc27tfwZRWNkSh0kU-WeMayl7IXL2qZbp_3nT3lq3r8E4MOABBxZArgcBgFxv-eWckVMg4d2th0GwqjmJk2lPTI)

To understand how a single feature can affect the output of the model we use a partial dependence plot where we plot SHAP value of that feature versus the value of the feature for all examples in a dataset.

‌ SHAP values represent a feature's responsibility for a change in the model output, the plot below represents the change in predicted output as RM changes. Vertical dispersion at a single value of RM represents interaction effects with other features. 

### **Summary Plot**

![Summary plot](https://lh5.googleusercontent.com/czqK1_0oVj4fU5OnnA49GcMEIGad7UhKJMNh7wCE9VGzezCSHb4ji1ts_S1atsLKwK6HJaAmdMRvYDfRaLxkMF-CiZpDEvsPDp5W-stufPJ124fxsOUo8cpaK44XXq49mxFbTfHS)

To understand which features contributed more to the model output prediction SHAP has something called summary plot.

![Summary plot](https://lh5.googleusercontent.com/iNdXT5IF0sVkDnfeFI0UBFpP0YDBR9xzX1rXj1n_g_l3SQc4m182ti-bmYWFusPRwhrTwJzA25HoE6SW87nnYsHVpGHhCPLgCw2-Z7_fhtRAZbH2kYLwBntyZsLdsk12LNqLKfoJ)

This is also a summary plot but here the exact values are plotted instead of absolute value.

Apart from this SHAP is even used for the deep learning models for image processing which is out of the scope of this book.  


