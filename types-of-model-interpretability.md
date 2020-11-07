# Methods of Model Interpretability

Before talking about the different methods/techniques for Model Interpretability, we need to mention the types of machine learning models. 

There are two types of models 

1. Interpretable Models
2. Black Box Models

![](.gitbook/assets/image%20%2896%29.png)

Interpretable Models are interpretable in itself. They don't require any other techniques to explain them explicitly. The other interpretable techniques can be applied to them also for interpreting the model but are not needed.  

Black Box Models are those which are not interpretable in itself. They require other methods to explain them. The reason why these models are called black-box is that they are very complex to understand or not understood at all. For example, when we consider a neural network model, there are millions of weights and calculations that are happening within the layers. Understanding them is extremely difficult and it is not possible for the human mind to understand such large calculations. Hence these models are called Black Models.

**Methods of Interpretability**

There are three methods employed for achieving Model Interpretability‌

1. Interpretable machine models
2. Model agonistic methods
3. Model specific methods

**Interpretable machine models:** These are models which are interpretable by themselves, without external methods. Example -[ Linear regression](interpretable-machine-learning-models/linear-regression/) and [Decision trees](interpretable-machine-learning-models/decision-trees/).

**Model agonistic methods:** These are the methods that can be employed to interpret any models. Example - [SHAP](model-agonistic-methods/shap.md), [LIME ](model-agonistic-methods/lime-and-k-lime.md)and [PDP](model-agonistic-methods/pdp.md).

