# Decision Tree
![image](https://regenerativetoday.com/wp-content/uploads/2022/04/dt.png)
This sub-repository mainly focuses on using Decision Tree Algorithm to solve classification problems.

---
## File descriptions
"Decision_Tree.ipynb" contains the describtion and coding of applications of decision tree algorithm.

Outline:
- Introduction
- Algorithm
    - Steps for creating a decision tree
    - Information Gain (IG)
    - The Formula of Inpurity of a node
        - Entropy
        - Gini Impurity
- Illustration
- Advantages and Disadvantages
    - Advantages
    - Disadvantages
- Code and Applications on data sets
    - Classification problem
    - Regression problem
- Reference

---

## A brief introduction
* [Introduction](#Introduction)
* [Entropy](#Entropy)
* [Gini Index](#Gini)
* [Information Gain](#IG)
* [Confusion Matrix](#Confution)

---
## Introduction  <a class="anchor" id="Introduction"></a>
Decision Trees (DTs) are a non-parametric supervised learning method used for classification and regression. The goal is to create a model that predicts the value of a target variable by learning simple decision rules inferred from the data features. A tree can be seen as a piecewise constant approximation.
## Entropy  <a class="anchor" id="Entropy"></a>
Entropy is a metric to measures the impurity, or uncertainty in data. The formula of entropy is 

<img src="https://latex.codecogs.com/svg.image?Entropy&space;=&space;\sum_{i=1}^c&space;-P_i&space;log_2&space;(P_i)" title="Entropy = \sum_{i=1}^c -P_i log_2 (P_i)" />

where <img src="https://latex.codecogs.com/svg.image?c" title="c" /> is the total number of classes and <img src="https://latex.codecogs.com/svg.image?P_i" title="P_i" /> is the probability of class <img src="https://latex.codecogs.com/svg.image?i" title="i" /> in the node.
## Gini Index <a class="anchor" id="Gini"></a>
Gini index is used to determine the impurity or purity when building a decision tree in the classification and regression tree (CART) algorithm. The formula of Gini index is

<img src="https://latex.codecogs.com/svg.image?Gini=&space;1&space;-&space;\sum_{i=1}^c&space;P_i^2" title="Gini= 1 - \sum_{i=1}^c P_i^2" />

where <img src="https://latex.codecogs.com/svg.image?c" title="c" /> is the total number of classes and <img src="https://latex.codecogs.com/svg.image?P_i" title="P_i" /> is the probability of class <img src="https://latex.codecogs.com/svg.image?i" title="i" /> in the node.
## Information Gain  <a class="anchor" id="IG"></a>
Information gain is used to decide which feature to split at each step when building the decision tree. A decision tree algorhtim would maximize the value of information gain, and thus, the split with the highest value of information gain will be selected. If a node <img src="https://latex.codecogs.com/svg.image?V" title="V" /> is split into <img src="https://latex.codecogs.com/svg.image?V_l" title="V_l" /> and <img src="https://latex.codecogs.com/svg.image?V_r" title="V_r" />, the formula of information gain is

<img src="https://latex.codecogs.com/svg.image?IG&space;=&space;Entropy(V)-w_l&space;\times&space;Entropy(V_l)&plus;w_r&space;\times&space;Entropy(V_r)" title="IG = Entropy(V)-w_l \times Entropy(V_l)+w_r \times Entropy(V_r)" />

where <img src="https://latex.codecogs.com/svg.image?w" title="w" /> is the weight, that <img src="https://latex.codecogs.com/svg.image?w_l=\frac&space;{|V_l|}{V}" title="w_l=\frac {|V_l|}{V}" /> and <img src="https://latex.codecogs.com/svg.image?w_r=\frac&space;{|V_r|}{V}" title="w_r=\frac {|V_r|}{V}" />.

## Confusion Matrix
A confusion matrix is a table used to describe the performance of a classification algorithom. It compares the actual values with those predicted by the model. 

There are four basic terms:

* True Positive: An outcome where the model correctly predicts the positive class.
* True Negative: An outcome where the model correctly predicts the negative class.
* False Positive: An outcome where the model incorrectly predicts the positive class.
* False Negative: An outcome where the model incorrectly predicts the negative class.

Based on these four terms, we can also calculate the Accuracy, Recall, Precious, and <img src="https://latex.codecogs.com/svg.image?F_1" title="F_1" /> score. These parameters can be used to evaluate the algorithm.

---

## Datasets
* Personal Key Indicators of Heart Disease
  The dataset contains 18 variables (9 booleans, 5 strings and 4 decimals). In machine learning projects, "HeartDisease" can be used as the explonatory variable, but note that the classes are heavily unbalanced.

