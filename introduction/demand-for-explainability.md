# Demand for Explainability

To understand why explainability is important in data science, let us take an example of diabetic retinopathy - a diabetes complication that affects eyes. It is caused by damage to the blood vessels of the light-sensitive tissue at the back of the eye \(retina\). Let's assume we use a Deep Learning model with Convolutional Neural Networks for classification of the normal eye from the diabetic eye. We can easily make a model that does a fairly good job with validation accuracy of 90%. Then, a few questions may arise - what did the model see in the image to classify it? Did the model look into the same diagnostic parts of the images as done by the doctors? Or did it do something else? This is a very important context wherein a person can lose eyesight if he/she is misdiagnosed \(if our model says the eye is fine but the eye was damaged, someone is going to be in big trouble!\). In such cases, explainability is meant to engender trust from a model.

![](https://lh4.googleusercontent.com/FtmX_tsjJEDYDK-kTuYCqdxp38hECeibPZFDjgGUSfwU2WAlTPZRxhdKNhDLhuF-6Y8dUI0LAMxBcpbx5Lg4R3KqR54OLIwbRGyr-ZC7_sTJNeSP4H6vRx6JFmwnbL_l0v1xdiE0)

### The demand for explainability arises because of the following:

![](../.gitbook/assets/image%20%2899%29.png)

#### **Trust** 

People who use a machine learning model should trust the model with its predictions and decisions. This is highly subjective and varies from individual to individual.

#### Transparency

Transparency refers to the requirement that the end-user can understand how a decision/prediction is made by the AI system. Essentially, this means that one should understand what a model predicts and if there is any bias in that decision. Correctional Offender Management Proﬁling for Alternative Sanctions \(COMPAS\), a widely used criminal risk assessment tool, found that its predictions were unreliable and racially biased. So, after gaining transparency, this insight revealed a bias in the model which was a crucial breakthrough for the company.

#### Quality

Not all models are 100 percent accurate and hence defining quality is important. It only makes sense for people to use a highly accurate model. To identify, log and articulate sources of error and uncertainty throughout the algorithm and its data sources helps understand the expected and worst-case implications and further aid mitigation procedures.

#### Accountability 

For decisions made by the model - who is accountable? The person who uses it or the person who built it? There should be a way to identify and assign the responsibility for a decision made by an AI system.

#### Fairness

How do we ensure that algorithmic decisions do not create discriminatory or unjust impacts when comparing across different demographics \(e.g. race, sex, etc\).

The above 5 factors are achieved by Model Interpretability. But the vice versa need not be true. If a model is able to provide all the above 5 factors, the model can still be un-interpretable.

To provide a complete explanation for any decision by a black-box model can be a tedious job. The explanations need to provide clarity on all the above-listed aspects and have mathematical and scientific proof. This has led to a new line of research – interpretability - loosely deﬁned as the science of comprehending what a model did.

**Reference**

1. [Validation of the Correctional Offender Management and Profiling Alternative Sanctions \(COMPAS\)](https://search.proquest.com/openview/0ead7ecbca0e1c0ac0fa16c26c6cc5c8/1?pq-origsite=gscholar&cbl=18750&diss=y) - Pierson, Ashley M.Fordham University

