# Linear model feature

### **Sparse Linear Models**

The examples of the linear model that we have chosen are fairly simple. But in reality there might not be just a handful of features, but hundreds or thousands. And a linear regression model’s interpretability goes downhill. There might be cases wherein there are more features than instances, and a standard linear model does not fit. The solution to this, is to introduce sparsity\(=few features\) in our model. There are techniques that help eliminate features through regularization. They simply help pick the most important features that can allow our model to predict well on training data and generalize well for out of sample data. Lasso and Ridge are two of the most common and widely used regularization techniques. A nice example of how they are implemented on a dataset in python is given in this [article](https://www.analyticsvidhya.com/blog/2016/01/ridge-lasso-regression-python-complete-tutorial/). Other methods that can be used for sparsity are Manually selected features, Univariate selection, Forward selection, Backward selection.  

