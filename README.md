# credit-risk-classification
Module 20 Challenge

# Module 12 Report Template

## Overview of the Analysis

* Create a predictive model to evaluate the risk to a financial institution of lending money to an individual.
* The model used details about the loan (interest rate and amount loaned) and details about the credit history of the individual (income, debt-to-income ratio, number of accounts, derogatory marks, and total debt) to predict risk.
* The training and testing data also included the ultimate outcome for each loan.
* The data was split into training and testing data. The training data was evaluated in a Logistic Regression algorithm and then testing data was evaluated against the model to determine the accuracy of the predictions.
* A second model was evaluated using a oversampling of failed loans to account for the disparity in outcomes (the original data had 75036 successfully repaid loans and 2500 failed loans).

## Results

* Machine Learning Model 1 (No oversampling):
  * Training data: 56277 successful, 1875 failed
  * Testing data: 18759 successful, 625 failed
  * Accuracy: 99%; Balanced Accuracy: 94%
  * Precision: 100% successful, 87% failed
  * Recall: 100% successful, 89% failed
  * 67 failed loans were incorrectly predicted to be successful, 88 successful loans were incorrectly predicted to fail

* Machine Learning Model 2 (Oversampling):
  * Training data: 56277 successful, 56277 failed
  * Testing data: 18759 successful, 625 failed
  * Accuracy: 100%; Balanced Accuracy: 100%
  * Precision: 100% successful, 87% failed
  * Recall: 100% successful, 100% failed
  * 2 failed loans were incorrectly predicted to be successful, 91 successful loans were incorrectly predictive to fail

## Summary

I would recommend the second model for use. Both models were nearly perfect at correctly predicting successful loans, but the second model was much better at predicting risky loans. It's important for a financial institution to reduce both declined loans that would ultimately be successfully repaid because that equates to a lost oppportunity for additioanl revenue. However, it is more important to reduce accepted loans that ultimately fail because that is just lost money. Between these two options, the number of loans that would have been declined but ultimately repaid is 11 out of 18759 evaluated (.0586%) in model 2, which is a tiny opportunity cost compared to approving 65 additional loans that end in default with model 1. The second model will be much better at protecting the financial institution from risk, while sacrificing a tiny amount of increased revenue oppurtunity.
