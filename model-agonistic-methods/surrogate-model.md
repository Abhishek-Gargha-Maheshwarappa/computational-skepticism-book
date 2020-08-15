# Surrogate model

**Introduction**

Surrogacy is a process when an external source is used to help achieve an outcome that was not possible internally. The early stage of applications of this technique in machine learning was when Mutual Angular Regularization was proposed to be surrogate to Latent Variable Modeling in 2015\([paper](https://arxiv.org/abs/1512.07336)\). The goal was to make the process and the outcome more interpretable. 

The core idea behind this technique is to get a simpler model to replicate the black-box model predictions as best as possible, and at the same time, provide interpretability. A common misconception is that if we are going to use a simpler model to interpret the black-box model, why make the black box model in the first place? Why can't we just make a directly interpretable model such as Linear Regression or Decision Tree?

The answer is because we will be comprising of accuracy. Though simpler models are easy to interpret, they are not very accurate with complex data. Complex models such as a deep learning model do a good job with complex data that a simple model would do. Our aim with surrogacy is to build a simple model, that can predict the prediction made by the black-box model.

The surrogate models can be applied globally or locally, based on the use case. In this section, we will discuss global surrogates, and in the next section, we will explain local surrogates. 

### Non-technical Explanation

The idea of surrogacy is very common outside model interpretability and has been used for decades. It is used widely in engineering systems and in the healthcare industry.

![](../.gitbook/assets/image%20%2835%29.png)

In healthcare, when a couple wants a child but cannot get the child on their own due to certain circumstances, they go for surrogacy i.e., get surrogate parent\(s\) for the child. In the above picture, we can see that a third person helps in giving the two parents a child. The father may or may not be the same. Eventually, the child is going to be raised in a family that might not be related by blood.

In a similar way, consider a black-box model to be the two green-colored parents \(see in pic\). The model cannot achieve interpretability by itself, just like the parents cannot get a child on their own. Hence, to achieve interpretability, or get a child, they take the help of an outsider. This outsider\( model/ the third person colored pink\) can help us achieve interpretability or get a child with ease. Hence, helping complete the goal seemed impossible earlier.

The above example is a perfect way of explaining the concept. We hope you feel the same and can remember the concept with this example. 

### Technical Explanation

By a simple interpretable model, we mean either a Linear model or a Decision tree or some other directly interpretable model which we will be adding in our "Interpretable Machine Learning models" section. We had mentioned that the simple models can help achieve global interpretability as well as local interpretability. What's the difference?

Global Interpretability aims to explain all the predictions made by the black-box model. Local Interpretability, on the other hand, aims to explain a single instance\(row\) or a subset of data predictions made by the black-box model. 

Global surrogacy is tough to achieve because a simple model needs to be trained to predict complex model predictions. The outcome is generally an overfit model that is interpretable. How do we achieve this high interpretability?

 Once we have a black-box model that is doing well, we make a new data frame with the independent features and the model predictions. Now, we train a directly interpretable model on this new data frame and our aim is to maximize accuracy. High accuracy simply means high accuracy in predicting the black-box model output. 

Once we have tunned the simple model to achieve maximum accuracy, we can visualize/interpret the simple model to gain interpretability on the black-box model.

### Visualizations

The Surrogate model visualizations are similar to that of the interpretable model that is used \(Linear regression, Decision tree, etc\). Below are some visualizations that can be done after making the surrogate model to evaluate the performance.  

![](../.gitbook/assets/image%20%28114%29.png)

![](../.gitbook/assets/image%20%2842%29.png)

![](../.gitbook/assets/image%20%28115%29.png)

In all the visualizations, you can see that the surrogate values slightly differ from the actual values. However, they still match the distribution and hence serve the purpose of Interpretability well. 

### Pros

* The technique helps achieve interpretability for any black-box model
* Straightforward mathematically and easy to implement - hence widely used

### Cons

* Tough to achieve high accuracy on complex models
* Tend to oversimplify a complex reality

  **Reference**

1. Molnar, Christoph. "Interpretable machine learning. A Guide for Making Black Box Models Explainable", 2019. [https://christophm.github.io/interpretable-ml-book/](https://christophm.github.io/interpretable-ml-book/).



