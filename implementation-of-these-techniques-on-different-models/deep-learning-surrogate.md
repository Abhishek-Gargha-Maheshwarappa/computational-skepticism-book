# Deep Learning - Surrogate

[Code Implementation Here](https://colab.research.google.com/drive/1OJJfqYsfg3Odi8aLC8Aw_UGE3EZzAH0w?usp=sharing)

### What is Deep Learning?

* Deep learning methods are based on artificial neural networks with representation learning
* They can be supervised, semi-supervised or unsupervised
* Architectures include deep neural networks, deep belief networks, recurrent neural networks and convolutional neural networks

### Making the Model

**Dataset:** Pima Indians Diabetes; **Target:** Outcome

The data is trained by making a Keras Sequential model with 3 layers.

**Accuracy:** 72.73% 

### **Implementation of Interpretability**

In this section, we will interpret a Keras Sequential model with a Decision Tree model as a surrogate. 

![](../.gitbook/assets/image%20%2889%29.png)

We found the best hyper-parameters for our DecisionTreeClassifier using GridSearch and then fit it on the training data without the outcome. The output column is replaced by the predictions made by the Keras Sequential model and then fit into the Decision Tree model.

### Visualizations

![](../.gitbook/assets/image%20%2893%29.png)

The above tree serves as a surrogate model to the Deep Learning model. As we can see, the most important feature is the root node i.e., Glucose.

There are 399 samples in the test set that are diabetic and 215 that are non-diabetic. If the person has low Glucose, then Age is the next most important feature. 

If the Glucose is high, then BMI is the next most important feature in determining if the person is diabetic or not.  

