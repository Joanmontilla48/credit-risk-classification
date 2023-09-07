## Credit Risk Classification

Machine learning techniques were employed to analyze a dataset containing historical lending data from a peer-to-peer lending company. The objective was to develop a model capable of assessing the creditworthiness of borrowers.

## Analysis Overview

The analysis considered various factors including Loan size, Interest rate, Borrower's income, Debt-to-income ratio, Number of borrower's accounts, Derogatory marks against the borrower and Total debt. The dataset, comprising 77,536 data points, was split into training and testing sets. The initial logistic regression model (Logistic Regression Model 1) was constructed using the scikit-learn LogisticRegression module. This model was applied to the testing dataset to predict whether a loan to a borrower would be classified as low-risk or high-risk, and the results are summarized below.

Initially, Logistic Regression Model 1 was trained on a dataset containing 75,036 low-risk loan data points and 2,500 high-risk data points. To address the class imbalance issue, the training data was resampled using the RandomOverSampler module from imbalanced-learn. This resampling generated 56,277 data points for both low-risk (0) and high-risk (1) loans, maintaining an equal representation of each class based on the original dataset.

The resampled data was then used to build a new logistic regression model, referred to as Logistic Regression Model 2, with the same purpose of predicting loan risk. The results for this model are also summarized below.

## Results

* Logistic Regression Model 1:
    * Precision: 93%
    * Accuracy: 94%
    * Recall: 95% 

* Logistic Regression Model 2:
    * Precision: 93%
    * Accuracy: 100%
    * Recall: 100%

## Summary

Logistic Regression Model 2 exhibits a lower likelihood of predicting false negatives. However, it is worth noting that, based on the confusion matrices for each model, Logistic Regression Model 2 tends to predict slightly more false positives (low-risk when the actual is high-risk).

If the primary goal of the model is to assess the likelihood of high-risk loans, neither model achieves precision above 90%. Nevertheless, Logistic Regression Model 2 outperforms Model 1 in terms of overall prediction accuracy and recall, making it the preferred choice due to its high accuracy and recall rates.