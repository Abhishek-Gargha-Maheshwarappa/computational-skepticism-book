# Model

### Encoding of Categorical Features

In our model, we have used One Hot encoding. But there are multiple ways to encode categorical features. If you want to have a look at the other ways, read [this](https://kiwidamien.github.io/encoding-categorical-variables.html). 

### One Hot Encoding

In this, we create a new feature per level of the original feature. The β per category is the estimated mean value of y for each category \(given all other feature values are zero or the reference category\). Note that the intercept has been omitted here so that a unique solution can be found for the linear model weights.

### Model Creation

Now that we have established the prerequisite knowledge and done some basic encoding required to build a Linear Regression model. Let us dive in and build a model for our dataset.

We want to make a model that will help us predict the charges given all the other features of an individual. You can refer to a step-by-step guide on how to build the model in our jupyter notebook on github. For now, all that is needed to be understood is that we have an OLS method to make our model. 

### **The summary of our OLS model is as below:** 

![OLS Summary](https://lh6.googleusercontent.com/il56OS6H1gdzHeV3SYgIrlBAhdROI_KdVhL_9YmGr0nQxvHvKBZe7ODfEQiZF6ktdU2RgDPBMKvtAS-fUcfANASlxK-o0SeFezdFEhCgS6zikRizH5xdEHm50zbMY9dONNHXmwdu)

The summary is indeed a very detailed one. To explain each and every metric of our summary will be a lengthy job. For the purpose of this book, we will only focus on the individual feature coefficients and t statistics for every feature. If you are interested in understanding the other metrics fully, you can read [this](https://medium.com/@jyotiyadav99111/statistics-how-should-i-interpret-results-of-ols-3bde1ebeec01).

Let’s have another look at the table more closely focused on the part we want to interpret.  


![OLS statistics](https://lh5.googleusercontent.com/BSRD-EVObfQ2Ukv8XSY6lklkHHKSAxLRbKhcfJLWhYBWpchsPZx7AJaUOnj3Lsj6Bvqk_hZU8Mx26PW-2ZMvWcf-CcWflInX3cgNnY6H3ITMZBYERqLqFdtQ0hCPMXGSU0PweA8R)

#### A simple way to interpret this model in form of an equation can be written as:

**charges =   
0.1886\*age + 0.0021\* female + 0.2012\*bmi + 0.0076\*children + 0.3801\*smoker                        -0.0504\*northeast - 0.0560\*northwest - 0.0669\*southeast - 0.0657\*southwest**

Interpretation of a numerical feature \(age\): An increase of the age by 1 unit increases the charges by the factor of 0.1886 when all other features remain fixed. This means that for an increase of 1 unit in age, the charges go up 1\*0.1886 = 0.1866. So there is an increase of 18.66% in the charges for every 1 year you age. Another reason to wish we could stay younger!

Interpretation of a categorical feature \(“smoker”\): The estimated number of charges is 0.38 times more for a smoker - again assuming that all other features do not change. So this means that a smoker will incur 38% more charges than a non-smoker. Another reason to quit smoking y’all.

All the interpretations always come with the footnote that “all other features remain the same”. This is because of the nature of linear regression models. The predicted target is a linear combination of the weighted features. The estimated linear equation is a hyperplane in the feature/target space \(a simple line in the case of a single feature\). The weights specify the slope \(gradient\) of the hyperplane in each direction. The good side is that the additivity isolates the interpretation of an individual feature effect from all other features. That is possible because all the feature effects \(= weight times feature value\) in the equation are combined with a plus. On the bad side of things, the interpretation ignores the joint distribution of the features. Increasing one feature, but not changing another, can lead to unrealistic or at least unlikely data points. For example increasing the number of rooms might be unrealistic without also increasing the size of a house.  
  


