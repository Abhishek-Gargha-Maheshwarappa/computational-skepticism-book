# SHAP \(SHapley Additive exPlanations\)

**Readers note:** _**The book is not yet completed will be released in the last week of August**_

### **Introduction**

In this section, we explore what is SHAP and how it will help us interpret a model. Given a sample and its prediction, SHAP decomposes the prediction additively between features using a game-theoretic approach.

Game theory was initially developed by John von Neumann and Oskar Morgenstern in 1944 as a mathematical theory. Following on from this, in 1944 Neumann published "The Theory of Games and Economic Behavior", co-authored with Morgenstern. This is considered to be one of the main foundation texts of game theory. But the economist John Nash, John Harsanyi, and Reinhard Selten received the Nobel Prize for Economics in 1994 for further developing game theory in relation to economics.

### Technical Explanation

#### Game theory

‌Game theory is the process of modeling the strategic interaction between two or more people in a situation containing set rules and outcomes in which each person's payoff is affected by the decision made by others. Game theory is used by the economist, political scientist, military and others.

![](https://gblobscdn.gitbook.com/assets%2F-MAC2Jbv5mGL5pUkLsG8%2Fsync%2Ff3f8943d2e1f2987432f7aab41a1647abd8b27d5.png?alt=media)

#### Non Cooperative Game theory

Non-Cooperative game theory is a competitive social interaction where there will be some winners and some losers. It is where Nash equilibrium comes into play. This book doesn't deal in detail about game theory. To read more about Nash equilibrium refer to an article from [Investopedia](https://www.investopedia.com/terms/n/nash-equilibrium.asp). The non-cooperative game theory is best understood with the example of the [Prisoner's Dilemma](https://www.investopedia.com/terms/p/prisoners-dilemma.asp).

#### Cooperative Game theory

Cooperative Game theory is where every player has agreed to work together towards a common goal. **Like/Unlike** the Nash equilibrium, cooperative game theory has shapely values. In-game theory, a coalition is what you call a group of players in a cooperative game.

#### Shapely values

A method of dividing up the gains or costs among players, according to value of their individual contributions .

It rests on three important pillars:

#### 1.Marginal contribution

The contribution of each player is determined by what is gained or lost by removing them from the Game. This is called their marginal contributions. To make it clear let us take an example.

‌Say every day you and your friends bake cookies. One day you get sick and don't go to bake cookies. That day, your friends produce 50 lesser cookies than they would have if you were there with them. So your marginal contribution to the coalition per day is 50 cookies.

#### 2.Interchangeable players have an equal value

If two parties bring the same things to the coalition, they should have to contribute the same amount and should be rewarded for their contributions.

#### 3.Dummy player has zero values

If a member of the coalition contributes nothing then they should receive nothing. But it might not be fair in all the cases, let us take an example to make this concept more clear.

‌If you go to a restaurant with friends and you order nothing and eat nothing, then there is no need for you to chip in on the bill. But in another scenario, when you are on maternity leave, and are not paid since you are not working, is not fair.

‌ Mathematically shapely values are represented by

![](https://gblobscdn.gitbook.com/assets%2F-MAC2Jbv5mGL5pUkLsG8%2Fsync%2Ff4fa557f5b9d49fb7abb54ea1ab29a6d77d76702.png?alt=media)

In a coalitional game, we have a set N of n players. We also have a function v that gives the value \(or payout\) for any subset of those players, i.e. let S be a subset of N, then v\(S\) gives you the value of that subset. So, for a coalitional game \(N, v\) we can use the equation to calculate the payout for player i, i.e. the Shapley value for any feature/column.

### **Non-technical Explanation**

Let us take an example and break it down to understand it better. Again, we will take the cookie example. Yes, you guessed it right, we love cookies too much.

Let us say David and Lisa are making cookies separately. David makes 10 cookies and Lisa makes 20 cookies.

![](https://gblobscdn.gitbook.com/assets%2F-MAC2Jbv5mGL5pUkLsG8%2Fsync%2F3b3009a9fa91155a349ccd9b76e716d975c5ef48.png?alt=media)



‌When David and Lisa working together, they streamline the process and are able to bake 40 cookies together.

![](https://gblobscdn.gitbook.com/assets%2F-MAC2Jbv5mGL5pUkLsG8%2Fsync%2F205ae6f0bc3cf539d424cdc47500d35765419d35.png?alt=media)

‌If we consider 1$ for each cookie, then they make $30 when they bake it separately \(30 cookies - David makes 10 and Lisa makes 20\). But when they bake together they get $40 \(40 cookies together\).

Let us now calculate the marginal contribution

#### Case 1

![](https://gblobscdn.gitbook.com/assets%2F-MAC2Jbv5mGL5pUkLsG8%2Fsync%2F04be9829c7c321e01faf5abc0bcc73bc8b90bea4.png?alt=media)

If David makes 10 cookies alone then, 40-10 = 30 

This is Lisa's marginal contribution to the coalition.

#### Case 2

![](https://gblobscdn.gitbook.com/assets%2F-MAC2Jbv5mGL5pUkLsG8%2Fsync%2Fbebe882ac75f49211b209f1028c9fa6f1670b580.png?alt=media)

If Lisa makes 20 cookies alone then, 40-20 = 20

This is the marginal contribution of David to the coalition.

So in the first case, David's value to the coalition is 10 cookies and in the second case, David's value to the coalition is 20 cookies. According to the Shapely equation, to find the Shapely value of David we need to average these two values i.e., \(10+20\)/2 = 15. This the  Shapely value for David

Similarly, for Lisa, in the first case the value to the coalition is 30 cookies. And in the second case, her value to the coalition is 20 cookies. So Shapley value for Lisa will be \(20+30\)/2 = 25.

We hope the above example have given clarity on what Shapely values are.

‌SHAP gives the feature importance assigned to every feature which will correspond to the contribution by it for the prediction.

SHAP can be applied to tabular data and image data. SHAP is a model agnostic method, which means it can be applied to any model.

### Visualizations

The various interpret abilities provided by SHAP are:

**1.Force Plot**

![](../.gitbook/assets/image%20%285%29.png)

The above interpretation shows how each feature is pushing or contributing to moving the base value \(the average model output over the training dataset\) of the output. Features that push prediction higher are shown in red and the features pushing the value lower are in blue.

#### **2.Partial Dependence Plot** 

![](https://lh5.googleusercontent.com/xpaILWMid_xyQ7viUNI8rD584-C1uvJMNsh0LTpREJh4VRtLHYc27tfwZRWNkSh0kU-WeMayl7IXL2qZbp_3nT3lq3r8E4MOABBxZArgcBgFxv-eWckVMg4d2th0GwqjmJk2lPTI)

To understand how a single feature can affect the output of the model we use a partial dependence plot where we plot the SHAP value of that feature versus the value of the feature for all examples in a dataset.

‌ SHAP values represent a feature's responsibility for a change in the model output, the plot below represents the change in predicted output as RM changes. Vertical dispersion at a single value of RM represents interaction effects with other features. 

#### **3. Summary Plot**

![Summary plot](https://lh5.googleusercontent.com/czqK1_0oVj4fU5OnnA49GcMEIGad7UhKJMNh7wCE9VGzezCSHb4ji1ts_S1atsLKwK6HJaAmdMRvYDfRaLxkMF-CiZpDEvsPDp5W-stufPJ124fxsOUo8cpaK44XXq49mxFbTfHS)

To understand which features contributed more to the model output prediction SHAP has something called summary plot.

![Summary plot](https://lh5.googleusercontent.com/iNdXT5IF0sVkDnfeFI0UBFpP0YDBR9xzX1rXj1n_g_l3SQc4m182ti-bmYWFusPRwhrTwJzA25HoE6SW87nnYsHVpGHhCPLgCw2-Z7_fhtRAZbH2kYLwBntyZsLdsk12LNqLKfoJ)

This is also a summary plot but here the exact values are plotted instead of absolute value.

### Algorithms suitable for SHAP application

SHAP is a model agnostic method that can be applied to any kind of model.

Currently, we are dealing with tabular data sets and in the upcoming version we will deal with computer vision and natural language processing models

### **Pros** 

* It is better than feature importance since it considers the coalition effect for calculating feature importance

### **Cons**

* To generate SHAP for all the data instance is computationally expensive for the large data set



  


