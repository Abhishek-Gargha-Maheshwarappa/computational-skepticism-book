# How does one achieve Interpretability?

So far we have seen that interpretability is something that is computationally less expensive than explainability. But how do we measure it? To answer this, let us understand the definition of Interpretability more clearly:

"Interpretability" in machine learning is the ability to predict a model's output before the model itself. If we can predict that a model will classify a text as spam/ham, for all possible texts in our training dataset, we have a full interpretation of our model. 

We must understand that there are no clear measures for measuring interpretability. That being said, there has been a lot of progress in this field. Google AI recently innovated TCAV  - a technique which allows an individual to test a model on concepts it has generated through training. Microsoft has also been working on interpretability with Azure Machine Learning Studio. Azure ML empowers developers and data scientists to make models and interpret them with great visualization tools, all on the cloud! 

Even though Interpretability has no exact measure, there are multiple methods to conclude an interpretation. It is important to understand here that there is no such thing as a partial interpretation. We either interpret a model's predictions or we don't. Hence, the need for a measure is insignificant. We need to be able to answer "how" to achieve "interpretability", rather than "how much", to actually achieve interpretability.

![](../.gitbook/assets/image%20%2885%29.png)

While companies continuously work to make innovative technological advancements in this field, traditional methods continue to provide a good base with model interpretation. These methods include Global surrogates, Feature interaction, PDPs, Shapley, LIME, etc. In this book, we will give a "hands-on" with a few of these methods. We have taken multiple datasets to interpret and coded in Python to demonstrate how to achieve interpretability. 

