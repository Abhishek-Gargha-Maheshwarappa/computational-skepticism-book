---
description: Meaning of important Stats...!!!
---

# Statistical Interpretation

### 

### **The summary of our OLS model is as below:** 

![OLS Summary](https://lh6.googleusercontent.com/il56OS6H1gdzHeV3SYgIrlBAhdROI_KdVhL_9YmGr0nQxvHvKBZe7ODfEQiZF6ktdU2RgDPBMKvtAS-fUcfANASlxK-o0SeFezdFEhCgS6zikRizH5xdEHm50zbMY9dONNHXmwdu)

The summary is indeed a very detailed one. To understand what features are significantly impacting our prediction, we will take a closer look at the "t" statistic or the "p" value. Both of these can help us decide if a feature is significant or not. 

In case of "t" statistic, if the value is below -2 or above +2, we can say that the feature is significant. Refer to the table above and we can observe that all features are significant except "sex" which has a t-value between -2 and +2. So this leads us to the conclusion that "sex" is not an important feature when building a linear model on this data.

Now we could go ahead and make the model with the remaining parameters, but we would ideally want to run the OLS again on the remaining features to ensure all significant parameters are present. On running the OLS again, we obtain the below table:

**Insert table with high p value for children** 

To our surprise, the table indicates that we may still be considering an insignificant feature in "children" which has a t value of \_\_\_\_\_\_\_\_\_. Let's run the OLS one more time, this time without "children".

![OLS Summary](../../.gitbook/assets/image%20%289%29.png)

All the t values are either below -2 or above +2. This confirms that these are the significant parameters in our data. Let's go on to interpret this table.

To explain each and every metric of our summary will be a lengthy job. For the purpose of this book, we will only focus on the individual feature coefficients and t statistics for every feature. If you are interested in understanding the other metrics fully, you can read [this](https://medium.com/@jyotiyadav99111/statistics-how-should-i-interpret-results-of-ols-3bde1ebeec01).

Let’s have another look at the table more closely focused on the part we want to interpret.  


![OLS Statistics](../../.gitbook/assets/image%20%287%29.png)

#### A simple way to interpret this model is in the form of an equation. It can be written as:

**charges =**  0.1899\*age + 0.2017\*bmi + 0.3807\*smoker - 0.0422\*northeast - 0.0470\*northwest - 0.0587\*southeast - 0.0568\*southwest

Interpretation of a numerical feature \(age\): An increase of the age by 1 unit increases the charges by the factor of 0.1899 \(when all other features remain fixed\). This means that for an increase of 1 unit in age, the charges go up 1\*0.1899 = 0.1899. So there is an increase of 18.99% in the charges for every 1 year you age. Another reason to wish we could stay younger!

Interpretation of a categorical feature \(“smoker”\): The estimated number of charges is 0.38 times more for a smoker - again assuming that all other features do not change. So this means that a smoker will incur 38% more charges than a non-smoker. Another reason to quit smoking y’all.

All the interpretations always come with the footnote that “all other features remain the same”. This is because of the nature of linear regression models. The predicted target is a linear combination of the weighted features. The estimated linear equation is a hyperplane in the feature/target space \(a simple line in the case of a single feature\). The weights specify the slope \(gradient\) of the hyperplane in each direction. The good side is that the additivity isolates the interpretation of an individual feature effect from all other features. That is possible because all the feature effects \(= weight times feature value\) in the equation are combined with a plus. On the bad side of things, the interpretation ignores the joint distribution of the features. Increasing one feature, but not changing another, can lead to unrealistic or at least unlikely data points. For example increasing the number of rooms might be unrealistic without also increasing the size of a house.  
  


