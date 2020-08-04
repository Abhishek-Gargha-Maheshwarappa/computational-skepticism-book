# Creating the model

**Readers note:** _**The book is not yet completed will be released in the last week of August**_

To demonstrate the application of Decision Tree model, we will consider Churn data set. Our aim is to be able to predict whether a customer will Churn or not, using a Decision Tree classifier. 

Before creating the model, we have included a few pre-processing step. 

Firstly, we have adjusted for missing values in the data by replacing with the mode for discrete \(categorical\) columns and mean for continuous \(numeric\) columns.

Secondly, to make the interpretation easy, we have reduced the data set using feature importance. In this step, we have essentially trained a Decision Tree classifier on the entire data set, and then calculated the feature importance for every column using the "model.feature\_importances\_" function \(inbuilt function\).

![Variable Importance](../../.gitbook/assets/image%20%2822%29.png)

After calculating the feature importance for every column, we have filtered out the columns that had a value lower than our threshold value. The threshold value chosen by us is 0.05, but this can be changed as per your convenience. 

Having filtered the unimportant columns, we remain with only four columns - Monthly Charges, Total Charges, Contract and Tenure. We have used these four columns to train our model.

One last step before we train our model is to ensure we use the right hyper parameters. There are multiple ways to find the right hyper parameters that would yield a highly accurate model. In our case, we have used Grid Search to find them. If you are interested in knowing how the Grid Search algorithms works, read this **article**. 

![Confusion Matrix for test data](../../.gitbook/assets/image%20%2820%29.png)

After running the model with the best hyperparameters from Grid Search, we get an accuracy of 76% on test set. This is actually pretty good! Especially because trees generally tend to over fit on training data and don't perform well on test data. 

