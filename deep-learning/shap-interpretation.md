---
description: Horse and Human classification Dataset
---

# SHAP

### **SHAP \(SHapley Additive exPlanations\)**

In this section we explore what is SHAP and how it will help us interpret a deep learning model. Given a sample and its prediction, SHAP decomposes the prediction additively between features using a game-theoretic approach.

Game theory was initially developed by John von Neumann and Oskar Morgenstern in 1944 as a mathematical theory. Following on from this, in 1944 Neumann published The Theory of Games and Economic Behavior co-authored with Morgenstern. This is considered to be one of the main foundation texts of game theory. But the economist John Nash, John Harsanyi, and Reinhard Selten received the Nobel Prize for Economics in 1994 for further developing game theory in relation to economics.

### Game theory

‌Game theory is the process of modeling the strategic interaction between two or more people in a situation containing set rules and outcomes in which each person's payoff is affected by the decision made by others. Game theory is used by the economist, political scientist, military and others.

![](../.gitbook/assets/screenshot-117.png)

#### Non Cooperative Game theory 

Non-Cooperative game theory is a competitive social interaction where there will be some winners and some losers. It is where Nash equilibrium comes into play. This doesn't deal in detail about game theory. To read more about nash equilibrium refer to an article from [Investopedia](https://www.investopedia.com/terms/n/nash-equilibrium.asp). The non-cooperative game theory is best understood with the example of the [Prisoner's Dilemma](https://www.investopedia.com/terms/p/prisoners-dilemma.asp).

#### Cooperative Game theory

Cooperative Game theory is where every player has agreed tp work together toward a common goal. Like nash equilibrium cooperative game theory has shapely values. In a game theory a coalition is what you call a group of players in a cooperative game..

#### Shapely values

A method of dividing up the gains or costs among player acording to value of their individual contributions . 

It rests on three important pillars 

#### Marginal contribution

The contribution of each player is determined by what is gained or lost by removing them from the Game. This is called their marginal contributions. To make it clear let us take an example.

‌ Say every day you and your friends bake cookies, one day you get sick due to eating too many cookies. That day group of your friends produces 50 lesser cookies than the days you were there. So your marginal contribution to the coalition per day is 50 cookies.

#### Interchangeable players has equal value

If two parties bring the same things to the coalition, they should have to contribute the same amount and should be rewarded for their contributions.

#### Dummy player have zero values

If a member of the coalition contributes nothing then they should receive nothing. But it might not be fair in all the cases, let us take an example to this thing more clear.

‌ If you go to restaurants with friends and you order nothing and eat nothing then there is no need for you to chip in on the bill. But in another scenario where you are on maternity leave and not paid since you are not working is not fair.

‌ Mathematically shapely values are represented by

![](../.gitbook/assets/shapely-value-formula.png)

In a coalitional game, we have a set N of n players. We also have a function v that gives the value \(or payout\) for any subset of those players, i.e. let S be a subset of N, then v\(S\) gives you the value of that subset. So, for a coalitional game \(N, v\) we can use the equation to calculate the payout for player i, i.e. the Shapley value.

Let us take an example and break it down to understand it better, so again we will take the cookie example. Yes, you guessed it right I love cookie too much.

Let us say David and Lisa are making cookies separately then David makes 10 cookies and Lisa makes 20 cookies.

‌When David and Lisa working together, they will streamline the process then they bake 40 cookies together.

‌ If we consider 1$ for each cookie then when they bake it separately it will 30 cookies so it will be 30$. But when they bake together they get 40$.

Let us now calculate the marginal contribution

if

It was introduced by Lundberg et al - who proposed a unified approach to interpreting model predictions.

‌‌Let us consider a project in a course that requires delivering 100 lines of code and consists of a team of 3 individuals who have worked as a team to present the project within a deadline to get good grades.

‌ Let us consider that James\(J\), Robert\(R\) and Susan\(S\) are the 3 members of the team.Then

| Students | Lines of code |
| :---: | :---: |
| J | 10 |
| R | 30 |
| S | 5 |
| JR | 50 |
| RS | 40 |
| SJ | 35 |
| JRS | 100 |





| Order | James contribution | Robert contribution | Susan Contribution |
| :---: | :---: | :---: | :---: |
| J,R,S | 10 | 40 | 50 |
| J,S,R | 10 | 60 | 30 |
| R,J,S | 20 | 30 | 50 |
| R,S,J | 65 | 30 | 5 |
| S,R,J | 35 | 60 | 5 |
| S,J,R | 65 | 30 | 5 |



| Contributor | Shapely Calculation | Shapely Value |
| :--- | :--- | :--- |
| James | 1/6\(10+10+20+65+35+65\) | 34.17 |
| Robert | 1/6\(40+60+30+30+60+30\) | 41.7 |
| Susan | 1/6\(50+30+50+5+5+5\) | 24.17 |

We have 3 students so the total combination is 3!\(3 factorial = 3\*2\) which is 6.

SHAP gives the feature importance assigned to every feature which will correspond to the contribution by it.

‌So our model predicts correct output but now to see what features in image influence this decision, we refer to the SHAP values.

![Shap Deep Explainer output](../.gitbook/assets/screenshot-85.png)

Red pixels increase the model's output while blue pixels decrease the output. The sum of the SHAP values equals the difference between the expected model output \(averaged over the background dataset\) and the current model output. The above image shows the features in the image that are contributing to the model output. Now, one can see this output and tell what actually leads the model to classify if the image has horse or human.

The corresponding python notebook is present in the github and one can try it hands on and understand its working practically and can play with notebook to understand better.

