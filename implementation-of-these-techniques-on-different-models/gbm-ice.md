# GBM - ICE

### What is GBM?

* Gradient Boosting Machine is a machine learning algorithm that forms an ensemble of weakly predicted decision trees
* It constructs a forward stage-wise additive model by implementing gradient descent in function space
* Also known as MART \(Multiple Additive Regression Trees\) and GBRT \(Gradient Boosted Regression Trees\)

### Making the Model

**Dataset:** Medical Cost Personal  ; **Target:** charges

The data is trained by calling the GradientBoostingClassifier function from Scikit learn Library

**Accuracy:** 

### **Implementation of Interpretability**

In this section we will interpret a GBM using ICE plots.

![](../.gitbook/assets/image%20%2872%29.png)



We use the Pycebox library and generate ICE plots for "Smoker" feature against out predicted output of "Charges"

### Visualizations

**ICE plot**

![](../.gitbook/assets/image%20%2883%29.png)

In the above plot, we see multiple lines plotted. Each line corresponds to a row in our data. We can see that for some individuals smoking does not affect the charges. But for a few of them, becoming a smoker seems to increase the charges. Such interpretation can be very useful in showing people the repercussions of smoking.



