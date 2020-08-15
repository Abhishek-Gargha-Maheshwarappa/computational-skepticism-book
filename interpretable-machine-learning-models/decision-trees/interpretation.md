# Interpretation

![Decision Tree Visualization](../../.gitbook/assets/image%20%2821%29.png)

Above is the Decision Tree classifier we have made for predicting churn. Can you interpret the tree from the first look?

Although Decision Trees look easy to interpret, to be able to understand the interpretations fully, is a tough task. In the above picture, we have a tree with three levels. Every level consists of a feature with a threshold value, entropy value for that node, count of samples included under that node, and the predicted values. 

To be able to explain the tree visualizations, we will only explain the leftmost nodes on every level. 

At the top of the tree, as a root node, we have "Contract &lt;= 0.5". This means that the Contract is the most important feature for our model. Note that all categorical columns have been coded to numeric values using Label Encoding. So a "0" in Contract means \*\*\*\*\*\* and a "1" means \_\_\_\_\_\_\_\_ 

**Insert category to code mapping**

Since Contract is a categorical column, it can only be "0" or "1", and not any value in between. From the root node, we can see that there are 5247 samples in our training set. The "class" and "value" in the root node are related wherein the former refers to the prediction and the latter shows the distribution of samples that in turn impact the prediction. the

The first element in "value" represents churn class "Yes" and the second element represents class "No". Whichever class has a higher number of samples in the value, is the predicted class for that node. 

![Root Node](../../.gitbook/assets/image%20%2823%29.png)

So in the root node, we have 3869 samples for churn class "Yes" and 1378 for churn class "No". Hence, the prediction class of this node is "Yes".  The entropy value is 0.831 which means it is not a pure node and has mixed samples. 

In the next level, we have two decision nodes based on whether Contract &lt;=0.5.

![Root Node and Level 1 of Decision Tree](../../.gitbook/assets/image%20%2825%29.png)

We can see that of the 5247 samples in the root node, 2862 have Contract = 0 \(**Categoryname**\) and 2385 have Contract = 1\(**Categoryname**\). In the first level after the root node, we have two decision nodes which show that "Monthly Charges" is the most important feature for that level. On the left, the decision threshold is "Monthly Charges &lt;= 68.975" and on the right, the decision threshold is "Monthly Charges &lt;=93.675". Remember that the primary separator of data before this node was Contract. 

In the left decision node, with 2862 samples, we have an entropy value of 0.985. Again, we can interpret that we have an impure node with mixed samples. Of the 2862 samples, 1637 have a prediction value of churn to be "Yes" and 1225 have a prediction value of churn to be "No". Since the majority are "Yes", the class associated to this node is Yes. 

In the right decision node, with 2385 samples, we have an entropy value of 0.344. This is very low compared to the previous entropy values. We can interpret that this is a more pure set than the ones before since the entropy value is close to 0. In support of this theory, we can see that 2232 points have churn "Yes" and only 153 have churn "No". Given the majority, the class associated with this node is "Yes" and the imbalance in values justify the low entropy value.

A similar interpretation can be done for every level and overall we can obtain an explanation with the decisions our model makes to generate a prediction. 

Note here that our tree has only 3 levels. This was because it had the best accuracy on the test set from all the other hyperparameter values. In essence, a tree with low levels will do well on test set but a tree with a high number of levels tends to overfit the training set and perform badly on tests.

