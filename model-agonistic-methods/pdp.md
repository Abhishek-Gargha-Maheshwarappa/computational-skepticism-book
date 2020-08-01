# PDP \(Partial Dependence Plot\)

The partial dependence plot shows the marginal effect of one or two features on the predicted outcome of a machine learning model. 

‌A partial dependence plot can show the relationship between the target and the features under investigation. 

‌Let us take the example of insurance where insurance charges are modeled on age, BMI, sex, smoker, region, and others. Here if we take a partial dependence plot for prediction versus age, then the partial dependence plot tells how prediction varies with respect to age averaging out all other features. 

‌PDP is a global method that considers all the data instances, it gives the global relationship of a feature with the predicted outcome. 

‌It can be applied with a maximum of two features due to the higher dimensional view is not possible to plot and understandable due limitation of the human perception. It is generally applied to the most important features and can have multiple PDPs side by side. 

