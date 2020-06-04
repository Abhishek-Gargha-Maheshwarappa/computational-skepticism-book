# Saliency Maps

### Introduction

In computer vision, a saliency map is an image that shows each pixel's unique quality. The goal of a saliency map is to simplify and/or change the representation of an image into something that is more meaningful and easier to analyze

Saliency maps for deep learning were first witnessed in the paper - Deep inside convolutional networks: Visualising Image classification models and saliency maps. \([Paper link](https://arxiv.org/abs/1312.6034)\)

The paper was presented by a group of researchers working on visual geometry at the University of Oxford. They highlighted visualisation techniques to compute images, saliency maps being one of them.

### Definition

Saliency can be defined as something that is different from its neighbours. Though most of the time it is used with visual context, it can also be an auditory or some other sensory stimuli.



![Saliency Example](https://lh5.googleusercontent.com/D1n5GtLejROOqbO7bpRZxVSHUEUOkYZ99XsHPIiSR26FY7_MfuWxo7E9cPRxTl4oqByzPgUETvA8kCQLQdSlWVu8fsEdmgM1HWCsjM8SdWxP0uwP1gY41z3Wh1MuuHzFlYRcjZsq)

In the above picture, the first row consists of original images and the second image shows the significant objects or regions, distinguished from the background. These are the salient regions.

### Non-Technical Explanation

There are 3 main factors that affect salience:

Properties of stimulus  
Context of stimuli  
Cognitive thinking of observer

#### Properties of stimulus

The properties can influence how saliency is perceived. Consider a small example - when we walk on the footpath and a sports bike like Hayabusa passes by on the road right next to us, we immediately notice the sound of exhaust, brightness and the majestic size of the vehicle.

#### Context of stimulus

The context plays a very important role in saliency. Take the above example of a bike, but this time in a different context - rather than a road , the bike is in a race. In this case, not many will notice the Hayabusa bike in detail because it’s common to bring a superbike to the race.

#### Cognition

By this, we simply mean perception. So to tell how bright, loud or appealing an object is depends on the person's emotions. Cognitive ability influences how we evaluate the world. A bike may be a relevant example for a person that loves bikes but might not be the right example for others.

With the combined effect of these three properties, it is possible to draw salience objects.

### Technical Explanation

There are multiple applications of Saliency maps that are used to process images to differentiate visual features in images. For example, a common practice in the fields of industrial and interior design is using infrared to detect temperature \(red colour is hot and blue is cold\). Another application is priority selection, e.g. to identify the most important information in visual input streams and to use this to improve performance in generating or transmitting visual data.

Saliency maps are essentially the first order derivative of the predicted class with respect to every pixel. We compute the gradient of the output prediction category with respect to the input image. 

   ∂\(output\) / ∂\(input pixel\)

This tells us how the output category prediction changes with respect to a change in input image pixels. The positive values in the gradients imply that a change to that pixel will increase the output value. These gradients highlight input regions that cause the most change in the output. As a result, we get the salient regions that contributed most towards the output highlighted.

By seeing how a change in a pixel can affect the probability of prediction class, we measure the importance of the pixel to prediction value. 

### Pros and Cons

There are multiple ways to draw saliency maps. Each method has their own pros and cons. For the current purpose of interpretability, we have generalized the pros and cons as below:

#### Pros

* Helps identify significant regions in an image for a model
* Easy to implement
* Easy to understand

#### Cons

* Different people can interpret the map differently 
* Saliency maps to not alter much with small tweaks in model - difficult to interpret in such situations



