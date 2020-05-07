# Interpretability

Before going to define the interpretability let's talk a little bit about the confusion between the terms Interpretability and explainability. There are a lot of papers which have different opinions about these two terms. Some define them to be different, while others define them to be the same. 

The oxford dictionary defines the word interpret as to explain the meaning of something and the word explains as to make an idea clear to someone by describing it in more detail. There is very little which separates interpretation from the word explanation unless we dive into the depth of literature. So to avoid all the confusion, interpretability, and explainability, we define the same.

### What is interpretability?

Miller defines Interpretability as the degree to which a human can understand the cause of a decision.Interpretable Machine Learning refers to machine learning models that can provide explanations regarding why certain predictions are made. 

The demand for interpretability arises when there is a mismatch between the formal objectives of the model and real-world costs in deployment settings.

Let's take an example of diabetic retinopathy, it is a diabetes complication that affects eyes. It's caused by damage to the blood vessels of the light-sensitive tissue at the back of the eye \(retina\).

![](https://lh4.googleusercontent.com/FtmX_tsjJEDYDK-kTuYCqdxp38hECeibPZFDjgGUSfwU2WAlTPZRxhdKNhDLhuF-6Y8dUI0LAMxBcpbx5Lg4R3KqR54OLIwbRGyr-ZC7_sTJNeSP4H6vRx6JFmwnbL_l0v1xdiE0)

Say you use Deep Learning with Convolutional Neural Networks for classification of normal eye from the diabetic eye, and the model does a fairly good job with validation accuracy of 90%. Then the question arises what did the model look into to classify the images, did the model look into the same diagnostic parts of the images used by the doctors or did it use something else. Because this is a very important context where a person can lose eyesight if he was misdiagnosed that his eyes were prefectly fine but in real not. So interpretability is meant to engender trust.  


## How does one achieve interpretability? 



There are no clear measures for measuring interpretability but there has been a lot of progress in this field. Google AI recently innovated TCAV which allows an individual to test a model on concepts it has generated through training. Microsoft has also been keeping up to trends with Azure Machine Learning Studio. Azure ML empowers developers and data scientists to make models and interpret them with great visualization tools, all on the cloud! While companies continuously work to make innovative technological advancements in this field, traditional methods continue to provide a good base with model interpretation. These methods include Global surrogates, Feature interaction, PDPs, Shapley, LIME, etc.  In this book, we will give a "hands on" with a few of these methods, namely - OLS, AzureML, LIME, SHAP and TCAV. We have taken multiple datasets to interpret and coded in python to demonstrate how to achieve interpretability. 

