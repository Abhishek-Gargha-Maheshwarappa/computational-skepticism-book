# Interpretability with Azure Machine Learning

This section of the book is something which both the authors find interesting. This section will help explain how you can get started and combine automated machine learning and model interpretability. 

Automated machine learning is a capability that allows a developer or data scientist to access an automated service that identifies the best machine learning pipelines for their labelled data. It empowers customers, with or without data science expertise, to identify an end-to-end machine learning pipeline for any problem.

In this section we will show how to explain why your model made the predictions it did with the various interpretability packages of the Azure Machine Learning Python SDK. 

#### Using the classes and methods in the SDK, you can get:

* Feature importance values for both raw and engineered features
* Interpretability on real-world datasets at scale, during training and inference.
* Interactive visualizations to aid you in the discovery of patterns in data and explanations at training time

The interpretability classes are made available through multiple SDK packages.

You can apply the interpretability classes and methods to understand the model’s global behavior or specific predictions. The former is called global explanation and the latter is called local explanation.

These methods can be also categorized based on whether the method is model agnostic or model specific. Different methods can target different types of models. The output is a set of information on how a given model makes its prediction. 

We have used material from Azure ML and Interpret-Community to make the contents of this section. Interpret Community incorporates community developed interpretability techniques under one roof with a unified set of data structures and visualization.

Before starting to code, we must understand that there are multiple experimental explainers available in the community. For our example, we will use Tabular Explainer.  


**Tabular Explainer is mostly used with tabular datasets. It currently employs the following logic to invoke the direct SHAP explainers:**  


| **Orginal Model** | **Invoked Explainer** |
| :--- | :--- |
| Tree-based Models | SHAP TreeExplainer |
| Deep Neural Network models | SHAP DeepExplainer |
| Linear Models | SHAP LinearExplainer |
| None of the above | SHAP KernelExplainer |

In the next section you will read about Tabular explainer and interpretability by tabular explainer.

