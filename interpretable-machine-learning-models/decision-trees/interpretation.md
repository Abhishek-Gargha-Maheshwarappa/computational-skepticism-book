# Interpretation

**Readers note:** _**The book is not yet completed will be released in the last week of August**_

![Decision Tree Visualization](../../.gitbook/assets/image%20%2821%29.png)

Above is the Decision Tree classifier we have made for predicting churn. Can you interpret the tree from first look?

Although Decision Trees look easy to interpret, to be able to understand the interpretations fully, is a tough task. In the above picture, we have a tree with three levels. Every level consists of a feature with threshold value, entropy value for that node, count of samples included under that node, and the predicted values. 

To be able to explain the tree visualizations, we will only explain the left most nodes on every level. 

At the top of the tree, as a root node, we have "Contract &lt;= 0.5". This means that Contract is the most important feature for our model. Note that all categorical columns have been coded to numeric values using Label Encoding. So a "0" in Contract means \*\*\*\*\*\* and a "1" means \_\_\_\_\_\_\_\_ 

**Insert category to code mapping**

Since Contract is a categorical column, it can only be "0" or "1" , and not any value in between. From the root node we can see that there are 5247 samples in our training set and 3869 of them have Contract = 0 and the remaining 1378 have Contract =1. The "class" in root node refers to the prediction. It can be either Yes or No.   

