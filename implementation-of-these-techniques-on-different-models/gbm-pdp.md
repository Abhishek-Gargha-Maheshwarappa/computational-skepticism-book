# GBM - PDP

[Code Implementation Here](https://colab.research.google.com/drive/1SiKKQ5T9rgrYjtDVEEraN1QZxTnztDF8?usp=sharing)

### What is GBM?

* Gradient Boosting Machine is a machine learning algorithm that forms an ensemble of weakly predicted decision trees
* It constructs a forward stage-wise additive model by implementing gradient descent in function space
* Also known as MART \(Multiple Additive Regression Trees\) and GBRT \(Gradient Boosted Regression Trees\)

### Making the Model

**Dataset:** Pima Indians Diabetes; **Target:** Outcome

The data is trained by calling the GradientBoostingClassifier function from Scikit learn Library

**Accuracy:** 

### **Implementation of Interpretability**

For this model, we will interpret with Partial Dependence Plots. 

![](../.gitbook/assets/image%20%2881%29.png)

With just few lines of code, we can plot the PDPs for any dataset using the sklearn partial\_dependence library.

### Visualizations

**PDP for every feature**

![](../.gitbook/assets/image%20%2880%29.png)

The above plot shows how change in output varies with variations in feature values. Some key points for interpretation from the above plots:

* As Pregnancies increase, the person's chances of becoming diabetic go up
* Higher the Glucose, higher the chances of person becoming diabetic
* BMI more than 25 increases an individuals chances of becoming diabetic

 **3-D PDPs**

![](../.gitbook/assets/image%20%2878%29.png)

These plots show the combined effect of two features on the change in output. As seen above, a reduction in both - Insulin and DiabetesPedigreeFunction, results in negative change of a person being diabetic \(nearing non-diabetic situation\).

**PDP interact plot**

The below plot shows the output prediction \(value inside square\) for every combination of values between the features Insulin and DiabetesPedigreeFunction\(values given by scale\). 

![](../.gitbook/assets/image%20%2875%29.png)

