---
description: How it is made ...!!!
---

# Model

In this section, we will take you through building a Linear Regression model. We will explain the steps very briefly as this part is not the focus of our book. We want to be sure of making a good accurate model because it makes no sense to try and interpret an inaccurate model.

The first and most important step in data modeling is actually ensuring having the right data. Data preparation for modeling is highly important and difficult to do. Most of the time of a data scientist's job is spent on data preparation rather than building the model.

During preprocessing, there are many steps to be followed starting with handling categorical columns. Categorical columns can be converted into a numerical encodes by Label encoding or split into multiple columns for every category \(1 if category is true, 0 if false\) by One-Hot encoding. In One-hot encoding, we create dummy variables for each category in the column and it leads to an increase in feature space. Label encoding converts categorical text data into model-understandable numerical data. To know more about the encoding refer to this link. 

For the data insurance premium data set, the data preparation used was encoding the categorical columns and scaling the data. Which is present in the hands-on notebook attached for this chapter.

After the data preparation, the linear regression model is trained on the training data. During the training, the model learns the slope and intercept to approximately fit the training data.

Different metrics like R2 square and Root Mean Squared Error are used to measure the model accuracy.

