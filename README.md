# Credit_Risk_Analysis

## Overview

### Purpose

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. We are using different techniques to train and evaluate models with unbalanced classes as we've been asked to use the imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.  We are evaluating the performance of these models to write a recommendation on whether they should be used to predict credit risk.

### Resources

- Python, pandas, numpy
  - sklearn.model_selection
  - imblearn.metrics
- LoanStats_2019Q1.csv
- screenshots

## Results

### Naive Random Oversampling

![1.JPG](https://github.com/mathur-nikita/Credit_Risk_Analysis/blob/main/screenshots/1.JPG)

Balanced accuracy score: 0.6573009382322703

High Risk Performance:
- precision: 0.01
- recall: 0.71

Low Risk Performance:
- precision: 1.00
- recall: 0.60

### SMOTE Oversampling

![2.JPG](https://github.com/mathur-nikita/Credit_Risk_Analysis/blob/main/screenshots/2.JPG)

Balanced accuracy score: 0.6622479600626106

High Risk Performance:
- precision: 0.01
- recall: 0.63

Low Risk Performance:
- precision: 1.00
- recall: 0.69

### Undersampling (Cluster Centroids)

![3.JPG](https://github.com/mathur-nikita/Credit_Risk_Analysis/blob/main/screenshots/3.JPG)

Balanced accuracy score: 0.5442661782548694

High Risk Performance:
- precision: 0.01
- recall: 0.69

Low Risk Performance:
- precision: 1.00
- recall: 0.40

### Combination (Over and Under) Sampling (SMOTEENN)

![4.JPG](https://github.com/mathur-nikita/Credit_Risk_Analysis/blob/main/screenshots/4.JPG)

Balanced accuracy score: 0.644711676499736

High Risk Performance:
- precision: 0.01
- recall: 0.72

Low Risk Performance:
- precision: 1.00
- recall: 0.57

### Balanced Random Forest Classifier

![5.JPG](https://github.com/mathur-nikita/Credit_Risk_Analysis/blob/main/screenshots/5.JPG)

Balanced accuracy score: 0.7885466545953005

High Risk Performance:
- precision: 0.03
- recall: 0.70

Low Risk Performance:
- precision: 1.00
- recall: 0.87

### Easy Ensemble AdaBoost Classifier

![6.JPG](https://github.com/mathur-nikita/Credit_Risk_Analysis/blob/main/screenshots/6.JPG)

Balanced accuracy score: 0.9316600714093861

High Risk Performance:
- precision: 0.09
- recall: 0.92

Low Risk Performance:
- precision: 1.00
- recall: 0.94

## Summary

Given that the formula for calculating F1 scores is F1 = 2(Precision * Sensitivity)/(Precision + Sensitivity), these are the following calculations:

Naive Random Oversampling:
- 0.01972222222
- 0.75

SMOTE Oversampling:
- 0.0196875
- 0.81656804733

Undersampling (Cluster Centroids):
- 0.01971428571
- 0.57142857142

Combination (Over and Under) Sampling (SMOTEENN):
- 0.01972602739
- 0.72611464968

Balanced Random Forest Classifier:
- 0.05753424657
- 0.93048128342

Easy Ensemble AdaBoost Classifier:
- 0.16396039604
- 0.96907216494

Given these calculations, the best forming model is the Easy Ensemble AdaBoost Classifier with a score of 0.96907216494, while the worst forming model is Cluster Centroid with a score of 0.57142857142.  The Easy Ensemble AdaBoost Classifier is recommended for predicting credit risk.
