# Credit_Risk_Analysis

## Overview 

### Purpose

The purpose of the loan prediction risk analysis is to evaluate the performance of logistic regression and ensemble models, and make a written recommendation on whether they should be used to predict credit risk.

### Methodology

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, this analysis will oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, the analysis will use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Lastly, the analysis will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 

## Results

### Oversampling Models

Native Random Oversampling
* Accuracy: 66%
* Precision: 99% overall (Low risk: 100%, High risk: 1%) - very low precision for predicting high risk files
* Recall: 66% overall ((Low risk: 66%, High risk: 67%) - consistent specificity across both outcomes

SMOTE
* Accuracy: 63%
* Precision: 99% overall (Low risk: 100%, High risk: 1%) - very low precision for predicting high risk files
* Recall: 62% overall ((Low risk: 62%, High risk: 64%) - consistent specificity across both outcomes

### Undersampling Model

ClusterCentroid
* Accuracy: 51%
* Precision: 99% overall (Low risk: 100%, High risk: 1%) - very low precision for predicting high risk files
* Recall: 56% overall ((Low risk: 56%, High risk: 46%) - high risk predictions are lower recall than low risk

### Combinatorial Model (Over- and Undersampling)

SMOTEENN
* Accuracy: 64%
* Precision: 99% overall (Low risk: 100%, High risk: 1%) - very low precision for predicting high risk files
* Recall: 70% overall ((Low risk: 70%, High risk: 57%) - high risk predictions are lower recall than low risk

### Ensemble Models

Random Forest
* Accuracy: 74%
* Precision: 99% overall (Low risk: 100%, High risk: 10%) - low precision for predicting high risk files
* Recall: 51% overall ((Low risk: 51%, High risk: 98%) - consistent specificity across both outcomes

Easy Ensemble
* Accuracy: 92%
* Precision: 99% overall (Low risk: 100%, High risk: 9%) - low precision for predicting high risk files
* Recall: 89% overall ((Low risk: 95%, High risk: 89%) - consistent high specificity across both outcomes


## Summary

Overall, all tested models had polarized low precision scores with very low precision for predicting high risk files. All testing models had varying recall scores that were more consistent across high risk and low risk predictions.

The model with the highest accuracy score is Easy Ensemble (92%), and lowest accuracy score is (51%).

### Model Recommendation

Easy Ensemble is the recommended model for the LendingClub credit card dataset because it has the highest accuracy and recall scores, which shows that the model has high prediction rates for both high risk and low risk files. This model has the bast results for predicting credit risk of all the tested models.