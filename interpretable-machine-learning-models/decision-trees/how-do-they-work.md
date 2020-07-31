# How Do They Work?

To understand the working of Decision Trees, consider the below table where we have four columns : Weather, Humidity, Wind speed and Run

![](../../.gitbook/assets/image%20%2817%29.png)

Our target variable is "Run" and the other three columns are our feature inputs.

To find the most important feature in the above table, we have to take into consideration a few metrics.





 How the decision tree will classify this

![Tree](../../.gitbook/assets/screenshot-278-.png)

As can be seen, the node Overcast is pure since it has only one output that is to go for a run. So we now know that if the weather is the overcast person will go for a run. But if the weather is not overcast then if it is rainy or sunny doesn't have an output, it has yes or no. So needs further splitting it deduce it more.

Till now you can consider the angel telling us which attribute to split on, now let us know how the angel knows which attribute to select.

**Which attribute to split on?**

It is based on the measure of the purity of the split, entropy helps to measure the purity of the split. Entropy is the way to measure the uncertainty of class in a subset. 

Explaining the terminology related to the decision is not in the scope of this book, these can be read from [ISLR](http://faculty.marshall.usc.edu/gareth-james/ISL/) 

