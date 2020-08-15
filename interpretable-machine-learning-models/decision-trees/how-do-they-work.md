# How Do They Work?

**Readers note:** _**The book is not yet completed will be released in the last week of August**_

To understand the working of Decision Trees, consider the below table where we have four columns : Weather, Humidity, Wind speed and Run

![](../../.gitbook/assets/image%20%2817%29.png)

We want to be able to predict when we can go for a run \(Run="Yes"\) and when we cannot\(Run="No"\), based on the Weather, Humidity and Wind speed. 

The Decision Tree algorithm works on a "Divide & Conquer" principle where the aim is to break the data into subsets with similar attributes. 

![](../../.gitbook/assets/image%20%2818%29.png)

As shown in the above figure, at the origin of the tree we have a "Root" node which is split into "Decision" and "Terminal" nodes. "Terminal" nodes are also referred to as "Leaf" nodes and they contain the model's predicted output. The "Decision" nodes essentially help in splitting the data into a subset. After splitting the data into subsets, we can have a common output for a subset \(terminal node\) or we can split the subset further into more subsets \(with the help of a decision node\)

**How do we decide our root node, decision nodes, and terminal nodes?** It depends on the function we choose to measure the quality of a split. 

Broadly, there are three functions that can be used: Gini, Chi-Squared, and Entropy. Every function has a mathematical formula linked to it and that mathematical formula is used to split the dataset into the root, decision, and terminal nodes. The most commonly used are Gini and Entropy. 

For the purpose of this book, we have explained the Entropy function. We have not shown the mathematical formula of the Entropy to keep things simple. If you are interested in knowing the mathematical functions or want to know how the other functions work, check out this **link**.

Before diving into the explanation of the Entropy function, it is important to understand the difference between a "Pure" node and an "Impure" node. Any "Decision" node that yields only a "Terminal" node, can be called a "Pure" node. In other words, the result of that decision is the same and common for all data points in that subset. 

![](../../.gitbook/assets/image%20%2892%29.png)

In the above picture, it can be seen that "Overcast" is a pure node because whenever the Weather is "Overcast", the predicted Run is "Yes". There is never a "No" Run when Weather is "Overcast". This is the definition of a pure node. If instead of the "Yes" in Run, we had all "No" for "Overcast", it would still be a pure node. Only if the data had a mixture of "Yes" and "No" run, with "Overcast" weather, would the node be termed as "impure?

With that definition in mind. Let's understand what Entropy is. 

Entropy can be defined as the measure of uncertainty of a class in a data/subset of a data set. Entropy essentially tells how pure/impure a node is. The purer a node, the higher it is placed in our tree. Using the **Entropy Mathematical Formula,**  we obtain the best attribute and use that as the root node of our tree.

Once we have the best attribute, we further split it into two child nodes based on next best attributes. At each step, we calculate the entropy for a node and then calculate the Information Gain. Overall, we want to design our tree in such a way that the Information Gain is maximized. The mathematical formula for the Information Gain is:

I.G. = Original Entropy - Subset1\(size\*entropy\) - Subset2 \(size \* entropy\)

So in our example, Weather was the best attribute and it yielded a pure node in "Overcast". If the Weather was "Sunny" or "Rainy", we would have further split the data into subsets as they are impure nodes. These subsets are made based on a mathematical calculation of Entropy and Information Gain for every attribute other than "Sunny" or "Rainy".

The process can continue untill we obtain a tree that will justify all the predictions in a dataset. If that is done, the tree would be too complex and it would overfit the data. By overfitting, we mean that the tree would only be able to predict correctly for the given data set and not new data. This is not desired and so it is advisable to avoid overly complex Decision Trees. In the next sections, we will show how to build a model using sklearn and interpret the model. All the mathematical calculations involved are done by the libraries function and all we have to do is define the hyper-parameters to our model. 

Explaining the terminology related to the decision is not in the scope of this book, these can be read from [ISLR](http://faculty.marshall.usc.edu/gareth-james/ISL/) 

