---
description: Horse and Human classification Dataset
---

# SHAP \(SHapley Additive exPlanations\)

### **SHAP \(SHapley Additive exPlanations\)**

SHAP is one of the local explanation methods that satisfies several desirable local explanation properties. Given a sample and its prediction, SHAP decomposes the prediction additively between features using a game-theoretic approach.

‌ It is introduced by Lundberg et al. who proposed a unified approach to interpreting model predictions.

‌ The convolutional neural network \(CNN\) is a class of deep learning neural networks and it represents an important part of computer vision application of image classification.

‌ Let us consider a project in a course that requires delivering 100 lines of code and consists of a team of 3 and has worked as a team present the project within a deadline to get grades.

‌ Let us consider James\(J\), Robert\(R\) and Susan\(S\) are the 3 members of the team.Then

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

We have 3 students so the total combination is 3! which is 6.

Shap gives the feature importance assigned to every feature which will correspond to the contribution by it.

‌ So the model predicts correct output but now to see what features in image influence this decision, this provided by the Shap values.

![Shap Deep Explainer output](../.gitbook/assets/screenshot-85.png)

Red pixels increase the model's output while blue pixels decrease the output. The sum of the SHAP values equals the difference between the expected model output \(averaged over the background dataset\) and the current model output. The above image shows the features in the image that are contributing to the model output. Now one can see this output and say what actually leads the model to classify the image has horse or human.

