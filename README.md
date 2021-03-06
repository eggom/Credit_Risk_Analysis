# Credit_Risk_Analysis
Module 1 Challenge - ML Pathway - Trilogy Instructors

**@Author:** Eduardo Gil González-Madroño
**@Date:** 20th Dec 2021

This is a brief summary and analysis of the performance of all the machine learning models used in this Challenge to predict risky loans over a collection of imbalanced data from the credit card credit dataset from LendingClub, a peer-to-peer lending services company.

Contents:

1. Overview of the analysis.
2. ML Algorithms Performance Results.
3. Summary.
<br>


## 1. Overview of the analysis.
<br>

The purpose of this analysis is, by using a heavily imbalanced dataset on risky and non risky credit card loans, build a Machine Learning Model (Classifier) that is able to deliver a good performance in recognizing a risky loand based on a number of featured that define the loan application.
<br>


## 2. ML Algorithms Performance Results.
<br>

It has been produced a total of X Classifiers with the following results on *Balanced Accuracy Score (BAS)* and *Precision / Recall*:

* Naive Random Oversampling + Logistic Regression :: 66.20 % BAS, 1% Precision, 72% Recall
* SMOTE Oversampling + Logistic Regression :: 65.68 % BAS, 1% Precision, 61% Recall
* Cluster Centroids Undersampling + Logistic Regression :: 54.47 % BAS, 1% Percision, 69% Recall
* SMOTEENN + Logistic Regression :: 61.94 % BAS, 1% Precision, 64% Recall
* BalancedRandomForestClassifier :: 78.85 % BAS, 3% Precision, 70% Recall
* EasyEnsembleClassifier :: Not Working due to issues with the dependencies

Below it can be seen the output of the classification_report_imbalanced for the <code>BalancedRandomForestClassifier</code> (as an example, as all reports can be seen on the notebooks):

<img src="./imgs/Capture_BalancedRandomClassifier_clf_report_imbalanced.JPG">
<br>


## 3. ML Algorithms Performance Results.
<br>

The overall results of the machine learning models are not really good to provide a high level of detection of risky credits. The Type I error and Type errors produced are high for the purpose of detecting high-risk credit without declining really good and healthy credits.

If to select one, it will be the one produced by <code>BalancedRandomForestClassifier</code> but again, its performance will be low to deploy it to a production environment.
