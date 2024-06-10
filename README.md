# credit-risk-classification
Module 20 Challenge - Credit Risk Classification

# Analysis Report of Credit Risk

## Overview of the Analysis

The intentions of the following predictive model was to train and evaluate historic lending data to build a model to identify the creditworthiness of borrowers.

The lending data include information on
1. Loan Sizes
2. Interest Rates
3. Borrower income
4. Debt to income
5. Number of Accounts
6. Derogatory Marks
7. Total debt
8. Loan Status

From the following data the goal was to predict the loan status.

To create the model with the ability to identify the creditworthiness of borrowers, various machine learning applications were applied to the data through sklearn including,
- confusion_matrix, 
- classification_report, 
- accuracy_score,
- train_test_split,
- LogisticRegression.

Train_test_split is used to allow for the data split into training and testing datasets.
This allows for untrained data to be used as testing to measure the accuracy performance.

The data is then fit to a Logistic Regression model before being evaluated with confusion matrix and Classification report to display.

The findings were that the Logistic Regression Model could predict at an accurate rate of 99.3% which is very near perfect. 
Overall the confused Matrix shows only 32 False Negatives + 86 False Positives, a total of 118 false predictions out of the total 19384.

The results of the classification report on the prediction model returned.

'0' Healthy loan
* Precision 1.0
* Recall 1.0
* Accuracy 1.0

'1' High-risk loan
* Precision 0.87
* Recall 0.95
* Accuracy 0.91

## Summary

Healthy loan predictions had a recall of 99.9% accuracy rounded to a score of 1.0.
This was achieved as only 86 loans of 18759 were incorrectly predicted as False positives translating that the loan was predicted incorrectly high-risk when it was healthy.

Furthermore, Healthy loans predictions had a precision score of 1.0 or 99.5% as 32 loans of the total 18759 were incorrectly predicted as healthy instead of high risk.

In reflection recall for High-Risk Loan predictions was 0.95 as out of the 625 High-Risk Loans, only 32 loans were incorrectly predicted as healthy [False negative].
Additionally, High Risk loan predictions had a precision of 0.87 as out of the total 625 actual High risks only 86 loans were incorrectly predicted as Healthy.

To conclude the results, the f1-score of 1.0 indicated a perfect logistic regression score for healthy loans and 0.91 for high-risk loans.
Once weighted to the number of healthy/high-risk loans, logistic regression score has an accuracy of 99%.

It is evident that the model is trained better in predicting healthy loans over high-risk loans but this is evident in how the actual data is weighted heavily towards healthy loans. Full implementation of the model is recommended regardless.
