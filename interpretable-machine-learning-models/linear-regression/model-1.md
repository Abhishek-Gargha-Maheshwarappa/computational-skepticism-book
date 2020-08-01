# Model

**Readers note:** _**The book is not yet completed will be released in the last week of August**_

In this section, we will take you through building a Linear Regression model. We will explain the steps very briefly as this part is not the focus of our book. We want to be sure of making a good accurate model because it makes no sense to try and interpret an inaccurate model.

The first and most important step in data modeling is actually ensuring having the right data. Data preparation for modeling is highly important and difficult to do. Most of the time of a data scientist's job is spent on data preparation rather than building the model.

During pre-processing, there are many steps to be followed - starting with handling categorical columns. Categorical columns can be converted into a numerical codes by Label encoding or split into multiple columns for every category by One-Hot encoding\(1 if category is true, 0 if false\). In One-Hot encoding, we create dummy variables for each category in the column and it leads to an increase in feature space. Label encoding, on the other hand, converts categorical text data into model-understandable numerical data. To know more about the encoding refer to this [link](https://towardsdatascience.com/understanding-feature-engineering-part-2-categorical-data-f54324193e63). 

For the Insurance Premium data set, the data preparation involved encoding the categorical columns and scaling the data. **Link to see how we did pre-processing**.

After the data preparation, a Linear Regression model is trained on the training data. During the training, the model learns the slope and intercept to approximately fit the training data.

The result of this training yields many different statistical metrics. The ability to understand these statistical metrics allows linear models to be interpretable. We will go through the statistical metric in more detail in the next section. 

