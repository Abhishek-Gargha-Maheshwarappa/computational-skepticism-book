# Random Forest - LIME

### **What is a Random Forest?**

* Random Forest is an ensemble learning method used for classification and regression 
* Random Forests are a modification of bagging technique that builds a large collection of non-correlated trees and then averages them
* This technique is sometimes even called "feature bagging".

  \*\*\*\*

### **Making the Model**

**Dataset:** Automotive marketing  ; **Target:** Customer ****lifetime value

The data is passed through pre-processing and then trained using Scikit learn Library with RandomForestRegressor function.

**R2 score:** 0.71

### **Implementation of Interpretability**

For this model we will be using LIME for interpretation. In particular, we use the LimeTabularExplainer which is part of the open source lime package.

![](../.gitbook/assets/image%20%2872%29.png)

We feed some data as shown above and then request the explainer to generate an explanation for a particular row. In the code, we have generated an explanation for 4th row and kept a cap on the number of features as 6.

![](../.gitbook/assets/image%20%2869%29.png)

### Visualizations

**Row Prediction**

![Predicted Customer Lifetime Value](../.gitbook/assets/image%20%2878%29.png)

**Positive/Negative Effects**

![](../.gitbook/assets/image%20%2875%29.png)

The above plot gives us an idea of the features that impact the prediction positively and negatively. By positive impact, we say that the feature brought the prediction closer to the predicted value. Negative effect implies the feature took the prediction away from the predicted value. The length of the bars also show the impact. Longer the bar, higher the impact. 

**Individual Feature Values**

![](../.gitbook/assets/image%20%2868%29.png)

The above plot shows the feature values for that particular row.

