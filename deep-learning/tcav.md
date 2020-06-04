# TCAV

### **Introduction**

TCAV is the latest breakthrough for model interpretability in the 21st century. It helps achieve interpretability beyond feature attribution. TCAV is short for Testing with Concept Activation Vectors. TCAV is an initiative by Google AI in a bid to make AI more responsible and transparent. 

In his keynote address at Google I/O 2019, Google CEO Sundar Pichai talked about how they are trying to build a more helpful Google for everyone which also includes building AI for everyone. 

TCAV is the latest breakthrough for model interpretability in the 21st century. It helps achieve interpretability beyond feature attribution. TCAV is short for Testing with Concept Activation Vectors. It is an initiative by Google AI, in a bid to make AI more responsible and transparent. 

TCAV allows quantitative testing with concept activation vectors to get model explanations.

### Definition 

TCAV gives quantitative explanations about how much a concept is important for predictions in a trained model. These can be used even with concepts that are not important to the trained model.

### Non technical Explanation

Let's take an example of evaluating how a kid identifies Elephants. We are not going into the details of how the kid learnt this differentiation. We are more keen to understand what concepts the kid has made in his/her mind with respect to an elephant.



![Elephant sideview](https://lh6.googleusercontent.com/RXxeBbYWQHCYAokvSaani1o-ihy795ZHQoK1LM2NfL_9bNTEvcEuVUvCTRZ99upo0JGa2m2fklKjpiQNekqV0CICdown5x3BGe3fvXERF5-lOSNTkX9fdBdeTdl9LvKE4p07wy0N)

We test the concepts by showing the kid 10 images of which 6 are elephants and 4 are other animals. The kid is super smart and correctly selects 5 elephants from the given 10 images. How did he miss the 6th one? We asked the kid why is the 6th image not an elephant? The kid replies - “Because he does not have a long face!”. This particular image was from a rear view and hence the kid went wrong. This tells us that the kid has used the elephant’s trunk as an important concept of classifying images as elephants. We can continue asking the kid more questions of “why” to understand some more concepts that their brain has built to identify an elephant. The TCAV score for trunk concept, in this case, is simply the ratio of the number images the kid correctly identified to the total number of images it was given i.e., 5/10.

### Technical Explanation

What is TCAV looking to achieve? To explain this, let's take the example of the Zebra classification.

![TCAV - Concept](https://lh5.googleusercontent.com/q2WVXwIMbhK2wO2PBMVigt9R6ofl486jvJORg7RdQNSiTglUlH5gLEWsAKom_jvJ-NLLWGN6Ya1zLh6Hts2yxiU4rw7gyKrAH99lXlEKUy-uAkDAZkD6UYgO4iAwXkdHkZo78kgn)

TCAV is like a microscope that latches on to a model and gives out a score which tells us whether the concept under study was important to the model. 

As shown in the above example, the model is trained to classify zebras and the concept  we chose to test was stripes. TCAV provides the quantitative importance of a concept if and only if the model network learned about it.

When we say we use stripes as a concept, we implement it and get the TCAV score by simply using the activation vectors for that concept. Hence, the name Test Concept with Activation Vectors.

A few prerequisites are needed for implementing TCAV. They are:  
Example images of the concept  
Random images  
Network under investigation and need access to the activation vectors of it

Once we are ready with these, what we need to do is build a linear classifier to separate the concept images from random images. Then, we take an orthogonal vector of the decision boundary. Now, we are ready with our CAV. 

So, a CAV is nothing but a direction pointing from away from the random image towards a more concept image. What are the next steps? 

Once we have a concept activation vector, the next step is to take the derivative of the probability of the class to the concept vector. This is the directional derivative with CAV.

The intuition behind all this is that if we consider a picture or pixel more like a concept than other concepts, then how much would the probability of being a Zebra changes? 

If it changes a lot, it's important or else it is not important.

This activity was done on many more zebra images to get a reliable explanation. The final TCAV score is simply a ratio of the zebra having stripes that positively increases the probability of being a zebra. In layman terms, it is like asking - for 100 images, how many of the images returned positive directional derivatives?

### Pros and Cons

#### Pros

* Address the subjectivity by bringing in quantitative methods
* Easy for the human to understand what model does globally

#### Cons

* Need ingredients like concept image and random image to develop CAV
* Difficulty in implementation compared other techniques like lime and saliency.

For more information refer Google [Tcav](https://research.google/pubs/pub47077/)



TO PUT OR NOT???

To understand how and why TCAV helps get to the next level of model interpretability, let’s take an example. If there is an image and every pixel of that image is an input feature then it is possible to look at every single pixel and infer their numerical values, which makes no sense to humans. We won’t say that the 5th pixel of this image has a value of 28, rather as humans we always say that there is a blue river in the picture. TCAV tries to overcome this issue and helps provide interpretability that is closer to the way humans interpret anything - through concepts \(even though they aren’t actually part of the training process\).

Typical interpretability methods restrict us to have one particular image that we are interested in understanding - such as LIME or SHAP. But TCAV gives an explanation that is generally true for a class of interest, beyond one image \(global explanation\).

### **TCAV Approach:**

So to understand the approach of how TCAV helps achieve concept activation in a model, consider the below image

![TCAV - Concept](https://lh5.googleusercontent.com/q2WVXwIMbhK2wO2PBMVigt9R6ofl486jvJORg7RdQNSiTglUlH5gLEWsAKom_jvJ-NLLWGN6Ya1zLh6Hts2yxiU4rw7gyKrAH99lXlEKUy-uAkDAZkD6UYgO4iAwXkdHkZo78kgn)

First, we see how an image of a zebra is fed as input to a trained machine learning model \(neural network\). The model tells the probability of whether or not the image is that of a zebra. Once we get this probability, we check if the striped concept is important to the zebra image classifier. TCAV helps get a score for how much the striped concept helped our model in classification. Note that we can only check this for concepts that actually our model has learned. 

The Concept Activation Vectors \(CAVs\), provide an interpretation of a neural net’s internal state in terms of human-friendly concepts. TCAV uses directional derivatives to quantify the degree to which a user-defined concept is important to a classification result–for example, how sensitive a prediction of “zebra” is to the presence of stripes.Consider that the neural network used in zebra classification consists of inputs x ∈ Rn and a feedforward layer l with m neurons, such that input inference and its layer l activations can be seen as a function :  


![](https://lh4.googleusercontent.com/PSyiap7-Zy3zytGUrmIwLcODCmTmCu-UBy8tiOoTWwbb1ATVejCr5j3VAv-87Ryo9nlsR4PGXAQBYWTjgkRsp8XBMVpkRz2NsrQRK6Njm4QbdSr_33XZpUvttkKyjKIdSzfkfF-T)

* a given set of examples that represent the stripes concept
* independent data set with the concept labelled 
* trained network
* CAVs are then learned by training a linear classifier to distinguish between the activations produced by a concept’s examples and examples in any layer
* TCAV uses the directional derivative SC,k,l\(x\) to quantify conceptual sensitivity

The first three steps help define a concept of interest and the next step helps make the vector. To define a “concept activation vector” \(or CAV\) we make the normal to a hyperplane separating examples without a concept and examples with a concept in the model’s activations. The last step is where the conceptual sensitivity is quantified. This directional derivative can quantitatively measure the sensitivity of model predictions with respect to concepts at any model layer.

This classifier vlc∊ Rm is a linear CAV for the concept C 

![TCAV](https://lh4.googleusercontent.com/Vt1lYFu1hatr1H0XgPjvkIbMETOd15m8peSNgUBtmoo-DPGtPZ85vFnsNuE-4E_93kZ-t0zwYJ-pMQLPDYAMdWBzIrLwc52wyHDd8FGhEtYfayX_zHE0ypimYyAYSGC6ya8mZqqb)

So hopefully we have helped give you a gist of how TCAV works conceptually and mathematically. 

With this understanding, let’s go ahead and understand our code implementation to get a “hand on” with this latest piece of technology advancement. We highly recommend that you go through the official documentation of TCAV

### **TCAV Implementation** 

For our implementation, we have used the CIFAR-10 dataset. It contains downscaled images of 10 different classes. 

We start off by defining our class of interest i.e., ships. We have labeled our class of interest as 1 and the others as 0. So x contains our input images and y contains our labels. Next, we make a train-test split on our original dataset, make a Keras sequential model with 4 convolutional layers. Once the model is trained, we proceed to make our TCAV object. 

We instantiate a TCAV object by calling ‘TCAV\(\)’ and assign our model to this object using the ‘set\_model’ method.

We then define the layer\(s\) of our model where we want to see the sensitivity of our concept. Note that we can only on the last activation/pooling/dropout layer. So, we have used the ‘split\_model’ on every layer possible i.e., after the activation for the first convolutional layer and after the dropout for every following convolutional layer.  
  
On training the tcav and calculating sensitivity for every split, we notice that the first, second and fourth layer have high sensitivity towards the ‘ocean’ concept. The third layer is slightly less sensitive. This could probably be because the layer is highly sensitive to other concepts such as the structure of the ship itself. How would we know if this hypothesis is true? We will have to try that out in another experiment to verify. 

So we can conclude by saying that the ‘ocean’ concept is highly important for our model to classify images of ships. Next time you see a ship, try not to think like a machine.

In the other example, we have demonstrated the sensitivity of the ‘cloud’ concept for classifying images of birds. 

TCAV has indeed opened doors for model interpretability in the modern era. We highly recommend that you experiment a bit with TCAV yourselves to become more fascinated by advancing technology. 

You can refer to tcav github to understand how to implement TCAV in your workflow.

For more information refer Google [Tcav](https://research.google/pubs/pub47077/)  
  


