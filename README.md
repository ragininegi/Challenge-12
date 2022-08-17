# Credit Risk Analysis


## Overview of the Analysis
Credit risk poses a classification problem that’s inherently imbalanced. This is because healthy loans easily outnumber risky loans.In this analysis, I  am using various techniques to train and evaluate models with imbalanced classes.



### I. The purpose of the analysis:
The purpose of this analysis is to determine if the assessment of the creditworthiness of borrowers on peer-to-peer lending platforms can be automated  using a classification model


### II. Dataset used and prediction variables:
Used dataset of historical lending activity from a peer-to-peer lending services company with the following input features:

   * loan_size
   * interest_rate
   * borrower_income
   * debt_to_income
   * num_of_accounts
   * derogatory_marks
   * total_debt
      
The output is `loan_status` column where 0 represents Healthy loans and 1 represents high risk loans


### III. Stages of Machine Learning:
1. Data Collection & data processing: using the dataset and splitting it as training set and testing set
2. Choosing a model- Logistic Regression: To categorize the riskiness of the loans as `high risk` and `healthy loans`,`logistic regression`is selected as        model
3. Training data: using the model, fitting the trained data
4. Prediction: using trained model to predict values for testing data
5. Evaluation: evaluating model's performance by doing the following:
   - Calculate the accuracy score of the model
   - Generate a confusion matrix
   - Generate classification report
6. Resampling Training Data: Oversampling the traning data as it is imbalanced data, by using `RandomOverSampler`
7. Train, Test & Evaluate the model with Resampled data: after this evaluation metrics is generated for `LogisticRegression` model


## IV. Results

The models are evaluated using accuracy, precision, and recall. The precision and recall values represent the label of interest

* Machine Learning Model 1: Linear Regression Model with Original training data

  * Accuracy: 0.95 (95%) given by balanced accuracy score, which indicates 95% of the predicted values are correct
  * Precision: For 0 label, the precision is 1 which indicates that the model is very good in identifying healthy loans and all healthy loans are correctly identified under label 0. For 1 label, the precision is 0.85(85%)which indicates that 85% of the values that the model predicted as high-risk are correct
  * Recall: For Label 1, the recall is 0.91(91%) which means of all the actual high risk loans(support value of 1 label is 619) the model rightly labelled 91% of them as high-risk. For label 0, the recall is 0.99 which inndicates that 99% of the values are rightly labelled


* Machine Learning Model 2: Linear Regression Model with Oversampled training data

  * Accuracy: 0.99 (99%) given by balanced accuracy score, which indicates 99% of the predicted values are correct
  * Precision: For 0 label, the precision is 1 which indicates that the model is very good in identifying healthy loans and all healthy loans are correctly identified under label 0. For 1 label, the precision is 0.84(84%)which indicates that 84% of the values that the model predicted as high-risk are correct
  * Recall: For Label 1, the recall is 0.99(99%) which means of all the actual high risk loans(support value of 1 label is 619) the model rightly labelled 99% of them as high-risk. For label 0, the recall is 0.99 which inndicates that 99% of the values are rightly labelled
  

## V. Summary

This model's objective is to accurately forecast high-risk loans among peer-to-peer lenders.

False negative is the number that needs to be reduced (predicted as Healthy but should be High-Risk).

The recall value depicts the proportion of hypothetical high-risk situations to actual high-risk cases. False negatives are reduced when recall value increases.

Both models have a 99% overall recall, however the dataset is biased due to the proportion of healthy loans to high-risk loans. Model 1 accurately predicts 83% of the recall value for the high-risk loans, while Model 2 correctly predicts 99%.

Model 2's total accuracy was 99%, up from Model 1's 95%.


---

## Technologies

It supports Python 3.7 and above and has been constructed in the jupyter lab notebook named `credit_risk_resampling.ipynb`
Additionally, the following packages/libraries are used to run the analysis:

- [pandas] - for analyzing data
- [jupyter]- for an IDE
- [numpy] - For numerical operations
- [sklearn.metrics]- for importing differnet metrics

---

## Installation Guide

Before running the application first install the following dependencies:

```python
  pip install pandas 
  pip install imbalanced-learn
  pip install pydotplus

```
--- 

## Contributors
Ragini Negi

Email : negiragini16@gmail.com <br>
LinkedIn : https://www.linkedin.com/in/ragininegi/

---

## License
Apache License 2.0

---
