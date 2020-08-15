# LIME \(Local Interpretable Model-Agnostic Explanations\)

### Introduction

In general, black-box models are highly complex and to be able to generate an overall global explanation for the model’s prediction is actually a very difficult job. The LIME algorithm was first brought into light for its ability to help understand image classification in 2016. With this algorithm, we could identify the parts of the input that triggered or affected our output the most.

LIME is short for Local Interpretable Model-Agnostic Explanations. It is a technique that can be applied to understand the predictions of a black-box model, by understanding the individual predictions with the help of a simpler, and directly interpretable model. 

LIME can be used in case of tabular, text and even image data. It generates a local explanation for a particular row, input word vector or a superpixel in all the three cases respectively. From the name, we can deduce that it is a model agnostic method - which means that this technique can be applied to any model. Also from the name, we can see that this generates Local Explanations. This means that this technique helps generate explanations for a single instance/row in our data set.

This technique is highly impactful when we want to focus on understanding individual predictions rather than a group of predictions made by a model. An example of such a use-case would be the healthcare industry, wherein each individual has a unique biological body mechanism. It would be wrong to generalize a model and assume the model would predict correctly for every human. Since every individual is unique, we would want to understand the single predictions and ensure that our model has not made a mistake. 

In the image below, we have a model that predicts if a person has the flu or not. For this particular individual, LIME indicates that sneeze and headache had contributed to the “flu” prediction, while “no fatigue” is evidence against it. With these, a doctor can make an informed decision about whether to trust the model’s prediction.

![LIME highlights the symptoms that led to the prediction](../.gitbook/assets/image%20%2826%29.png)

### Non-technical Explanation

Suppose we use a model to predict the number of daily confirmed COVID-19 cases for a particular state. Let’s assume that this “black box” model was made by a group of intellectuals that got accurate data from the government and the model has high accuracy on test data. So now, let’s say that our model predicted that the number of daily cases would be 300 in exactly a month’s time. The globally important features for our model predictions are: Previous weeks confirmed cases, number of people currently admitted in state’s hospitals, number of doctors available in state’s hospitals, and the number of recoveries in the previous 7 days. There are more features/ columns of data available with us like the number of public places currently opened, age and gender of the people who have had the virus. But for our model, these were the most important in making a prediction.  

![](../.gitbook/assets/image%20%2828%29.png)

A month later, in reality, the state observes the number of positive cases is up to 500. How could the model have gone so wrong? To understand this prediction, we could use the LIME technique and interpret what factors affected our model’s prediction. 

With the aid of good visualizations, we can find out the dates when our model predictions had started becoming inaccurate. Now, we can use LIME on the prediction of the earliest date wherein we observed this mismatch. On further diagnosis, we see that the model had made the prediction largely impacted by the feature - the number of public places currently open. So a less important feature had impacted our prediction. Why? This day was exactly 1 week past the day the government had eased the lockdown restrictions - why of course! So the number of public places had gone up in the past one week and even though the model had taken that into account, the model had actually worked on insufficient data to be able to predict the right number. This interpretation helped the intellectuals realize the need to collect more data. Maybe we need to include the number of people going to these public places? Well, that’s something which they will work on and decide.

Hopefully, the above example has helped establish the answer to how the LIME technique can be implemented to achieve interpretability and improve our model. 

### Technical Explanation

LIME uses the local fidelity criterion. This means that any explanation generated using LIME must correspond to the vicinity of the instance being predicted. To create this vicinity, LIME perturbs the instance being predicted. 

 

![](../.gitbook/assets/image%20%2827%29.png)

The above image is a toy example presented in the original [paper](https://arxiv.org/abs/1602.04938). In the example, LIME is used to generate an explanation for a single instance marked as a "bold cross". The other red cross and blue circles are sample instances in our data set that are in the vicinity of the instance corresponding to the prediction explanation \(the bold cross\). 

In the image, the proximity is represented by the size of the cross and the circles. The larger the cross or the circle, the closer it is to the instance under investigation. The dashed line represents a linear explanation that is locally true. 

We have to understand that features that may seem important locally need not be important globally. By global importance, we mean that a feature is important for all the instance predictions in the data set. But in local importance, the features may or may not be the same as global because only a single instance prediction is taken into consideration.

### Visualizations

![](../.gitbook/assets/image%20%28118%29.png)

![](../.gitbook/assets/image%20%28117%29.png)

![](../.gitbook/assets/image%20%28116%29.png)

### **Pros** 

* The technique can be applied to tabular, text and image data
* The technique can be easily used as it is implemented in a Python library \([lime.py](https://github.com/marcotcr/lime)\)

### **Cons**

* The vicinity of a prediction can vary and find the right  kernel width that generates an accurate local explanation is a difficult job
* The technique is inconsistent and there is often instability in the explanations





