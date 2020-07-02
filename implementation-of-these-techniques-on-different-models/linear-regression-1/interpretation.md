---
description: >-
  The interpretation of a weight in the linear regression model depends on the
  type of the corresponding feature (inputs)
---

# Interpretation

### Numerical feature:

The interpretation of a numerical feature is fairly simple. We can simply say that increasing the numerical feature by one unit changes the estimated outcome by its weight. An example of a numerical feature in the Medical cost dataset is the age of the individual.

### Binary feature: 

This is a feature that takes one of two possible categories for each instance. Examples of such a feature are the features “sex” or “smoker” in our Medical cost dataset. A reference category is selected and encoded to 0 \(male/non-smoker\) and 1 is used for the other category \(female/smoker\). Changing the feature from the reference category to the other category changes the estimated outcome by the feature’s weight.

### Categorical feature with multiple categories: 

Features with a fixed number of possible values fall under categorical features. An example is the feature “region”, with possible categories “northeast”, “northwest”, “southeast” and “southwest”. A solution to deal with many categories is the one-hot-encoding, meaning that each category has its own binary column. For a categorical feature with L categories, you only need L-1 columns, because the L-th column would have redundant information \(e.g. when columns 1 to L-1 all have value 0 for one instance, we know that the categorical feature of this instance takes on category L\). The interpretation for each category is then the same as the interpretation for binary features. We have implemented this in our code and you can have a look as to how it's done in our github repository.

### Intercept β0

The intercept is the feature weight for the “constant feature”, which is always 1 for all instances. Most software packages automatically add this “1”-feature to estimate the intercept. The interpretation is: For instance with all numerical feature values at zero and the categorical feature values at the reference categories, the model prediction is the intercept weight. The interpretation of the intercept is usually not relevant because instances with all features values at zero often make no sense. The interpretation is only meaningful when the features have been standardised \(mean of zero, the standard deviation of one\). Then the intercept reflects the predicted outcome of an instance where all features are at their mean value.



