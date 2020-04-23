# LIME

In this section, we will use LIME to understand how images are classified in our horse and human dataset. LIME is short for Local Interpretable Model-agnostic Explanations. This helps us generate explanations for image classification. It can be used on any model and helps generate local explanations i.e., instance specific explanations rather than global explanations. 

In the horse-human images dataset, we will use LIME to understand how our deep learning model distinguishes between the two categories. We aim to be able to understand what parts of the image are telling our model whether it is of a human or a horse.

If you have a look at the jupyter notebook on our github, you can see how we have built a Keras sequential model with 4 convolutional layers. Our model is trained over 30 epochs and is highly accurate in classifying images from our test dataset as human or horses. 

We have used LimeImageExplainer from the lime package and skimage - a python library for getting access to the image processing primitives, to generate our explanations. 

The LimeImageExplainer has a method ‘explain\_instance’ which takes in an input image as instance. For our example, we have taken the image of a famous Bollywood actress who is also a former Miss World - Aishwarya Rai Bacchan. We have not used this image previously for training our model and will be testing and interpreting our result with this image. 

Our explainer generates neighborhood data by randomly perturbing features from the instance. It then learns locally weighted linear models on this neighborhood data to explain each of the classes in an interpretable way \(see lime package [documentation](https://lime-ml.readthedocs.io/en/latest/lime.html)\). Using the explainer, we generate an explanation object with the corresponding explanations. This explanation object is of the type -  lime.lime\_image.ImageExplanation

Next, we call another method ‘get\_image\_and\_mask’ which takes in a label to explain \(in our case the label is human\). We set the below mentioned parameters in our method call:

Positive\_only: set to true so that it only takes superpixels that contribute to the prediction of the label. Otherwise, it will use the top num\_features superpixels, which can be positive or negative towards the label

Hide\_rest: set to 0 \(false\) to display the colored non-explanation part of the return image. If true, it would be gray

Num\_features: number of superpixels to include in explanation \(default is 5\)

This method returns a \(image, mask\), where image is a 3d numpy array and mask is a 2d numpy array that can be used with skimage.segmentation.mark\_boundaries.  


![Aiswaraya Rai](https://lh4.googleusercontent.com/89MB9hZwIURRtemWx7u1sNhbBsaQQRlpE5IQorQB1mBckjKzgAQKHX1qPtuO10lIA3kP1IyiTuTQdUj2ndvXmWV8RbxaM_mUoPRRjVqo6QHfnIQRyeop-gVcs2nfgCIn3QSnYT2I)

Mark\_boundaries returns an image in which the boundaries between labels are superimposed on the original image. \(Notice the yellow marker segregating our image into two\)

We have experimented with our parameters in the method calls so that we can observe the parts of the image that are positively affecting our label as green and the parts of our image that are negatively affecting our label. \(Notice the positive\_only has been set to false\)  


![Output of Lime](https://lh5.googleusercontent.com/WbtcKXgHKXqh-fIPTxnNlVmc7Zk1vmzD_LrlPUrKOftVytXUgWoej5Aj80ChNkmqwT1h60u-xEYbYyDGnsBoe_mxH-fTIZJ4qol99ci0pptBeZZKHk5k2wjkbCZetePbPpqbQjwp)

We can infer that the face of the human is being used by our model to classify the image as that of a human.

The same activity is then carried out for an image of a horse.  


![Horse](https://lh4.googleusercontent.com/3ABxEFtaTQkt_RaA3VhD8J114yfOuBEOSBApYAYQmyLuOA5x-EZ-wjMDxLUtSaSSVXKuUt-evu9vx6dhMZSB05IeOGMGXNNf0_zdZcjoOrqXTBZe7g8XtahgYII7IyWtkLfkCx3j)

You can observe that the head and tail of the horse are contributing positively to labeling the image as a horse. 

This technique is highly useful in cases where we want to understand why our model made a certain prediction. If our model is not working properly, this technique helps us identify the reasons why that might be happening.  


