# Tabular Explainer

TabularExplainer calls one of the four SHAP explainers underneath \(TreeExplainer, DeepExplainer, LinearExplainer, or KernelExplainer\), and automatically selects the most appropriate one for our use case. We can however, call each of its four underlying explainers directly. 

This explainer will help us make an Explanation dashboard which gives global and local visualizations to help interpret our model. 

Ok, so now that we have a brief idea of how automated machine learning helps achieve interpretability, let’s dive into some code and interpret some models!

You can refer to the code in our github. Here, we will show the visualizations achieved with the code. \(Be sure to run pip install azure ml-interpret before running the code\)

### Explanation Dashboard looks like:

| Plot | Description |
| :--- | :--- |
| Data Exploration | An oreview of the dataset along with prediction values. |
| Global Importance | Shows the top K\(configurable K\) important features globally. This chart is useful for understanding the global behavior of underlying model. |
| Explanation Exploration | Demonstrates how a feature is responsible for making a change in model's predicition values\(or probability of predicition values\) |
| Summary | Uses a signed local feature importance values across all data points to show the distribution of the impact each feature has on predicition value. |

###  

