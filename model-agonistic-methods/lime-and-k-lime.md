# LIME \(Local Interpretable Model-Agnostic Explanations\)

### What is it?

LIME is short for Local Interpretable Model-Agnostic Explanations \(LIME\). From the name, we can deduce that it is a model agnostic method - which means that this technique can be applied to any model. Also from the name, we can see that this generates Local Explanations. 

LIME is a technique that can be applied to understand the predictions of a black box model, by understanding the individual predictions with the help of a simpler, and directly interpretable model. Essentially, LIME helps understand a model, not by explaining all the predictions together, rather explaining the prediction of a single instance of data. This instance of data could be any point for which the user wants to understand the logic behind the model’s prediction. 

LIME can be used in case of tabular, text and even image data. It generates local explanation for a particular row, input word vector or a super pixel in all the three cases respectively. 

### Why LIME? 

In general, black box models are highly complex and to be able to generate an overall global explanation for the model’s prediction is actually a very difficult job. The LIME algorithm was first brought into light for its ability to help understand image classification in 2016 \[paper\]. With this algorithm, we could identify the parts of the input that triggered or affected our output the most. Even though this algorithm might not allow high volume of interpretability on model predictions, it definitely allows us to get a high quality in the local interpretation. This technique is highly impactful when we want to focus on understanding individual predictions rather than a group of predictions made by a model. An example of such a use-case would be the healthcare industry, wherein each individual has a unique biological body mechanism. It would be wrong to generalize a model and assume the model would predict correctly for every human. Since every individual is unique, we would want to understand the single predictions and ensure that our model has not made a mistake. 

### How LIME?

We will not be diving into the technical aspects of how to implement the LIME algorithm. Rather, with the use of a metaphorical example, we will help build an analogy and explain how the algorithm works. 

Suppose we use a model to predict the number daily confirmed COVID-19 cases for a particular state. Let’s assume that this “black box” model was made by a group of intellectuals that got accurate data from the government and the model has a high accuracy on test data. So now, let’s say that our model predicted that the number of daily cases would be 300 in exactly a month’s time. The globally important features for our model predictions are: Previous weeks confirmed cases, number of people currently admitted in state’s hospitals, number of doctors available in state’s hospitals, and the number of recoveries in the previous 7 days. There are more features/ columns of data available with us like the number of public places currently opened, age and gender of the people who have had the virus. But for our model, these were the most important in making a prediction.  

A month later, in reality, the state observes the number of positive cases is up to 500. How could the model have gone so wrong? To understand this prediction, we could use the LIME technique and interpret what factors affected our model’s prediction. 

With the aid of good visualizations, we can find out the dates when our model predictions had started becoming inaccurate. Now, we can use LIME on the prediction of the earliest date wherein we observed this mismatch. On further diagnosis, we see that the model had made the prediction largely impacted by the feature - number of public places currently open. So a less important feature had impacted our prediction. Why? This day was exactly 1 week past the day the government had eased the lockdown restrictions - why ofcourse! So the number of public places had gone up in the past one week and even though the model had taken that into account, the model had actually worked on insufficient data to be able to predict the right number. This interpretation helped the intellectuals realize the need to collect more data. Maybe we need to include the number of people going to these public places? Well, that’s something which they will work on and decide.

Hopefully the above example has helped establish the answer to how the LIME technique can be implemented to achieve interpretability and improve our model. 



