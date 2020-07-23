---
description: How it is made ...!!!
---

# Model

The important step in data modeling is data preparation for modeling. Most of the data scientist time is spent on data preparation rather than building the model.

During preprocessing there are many steps to be followed starting with handling categorical columns which should be converted into a numerical encodes by one-hot encoding or Label encoding. One-hot encoding is done by creating dummy variables for each category in the column and it leads to an increase in feature space. Label encoding converts this kind of categorical text data into model-understandable numerical data. To know more about the encoding refer to this link. 

For the data insurance premium data set, the data preparation used was encoding the categorical columns and scaling the data. Which is present in the hands-on notebook attached for this chapter.

After the data preparation, the linear regression model is trained on the training data. During the training, the model learns the slope and intercept to approximately fit the training data.

Different metrics like R2 square and Root Mean Squared Error are used to measure the model accuracy.

