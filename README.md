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
1. Data collection and processing involve dividing the dataset into a training set and a testing set.
2. Choosing a model: Logistic regression is used as the model to classify the riskiness of the loans as "high risk" and "healthy loans."
3. Training data: fitting the trained data using the model.
4. Making predictions using a trained model to test data
5. Evaluation: Assess the performance of the model by performing the following:
- Create a confusion matrix;
- Determine the model's accuracy score;
- Create a classification report.
6. Resampling Training Data: Using "RandomOverSampler," oversample the training data since it is unbalanced.
7. After training, testing, and evaluating the model using resampled data, evaluation metrics for the "LogisticRegression" model are produced.


## IV. Results

The models are evaluated using accuracy, precision, and recall. The precision and recall values represent the label of interest

Model 1 for Machine Learning: Linear Regression Using Initial Training Data

* According to the balanced accuracy score, 95% of the anticipated values are accurate, or accuracy: 0.95 (95%)
* Precision: For a label of 0, the precision is 1, meaning that all healthy loans are accurately identified under label 0. This shows that the model is highly good at recognizing healthy loans. The precision for one label is 0.85(85%), meaning that 85% of the values the model predicted as high-risk are accurate.
* Recall: For Label 1, the recall is 0.91 (91%), meaning that the model correctly identified 91% of the real high-risk loans (the support value for 1 label is 619) as such. Recall for label 0 is 0.99, meaning that 99% of the values are accurate.

Machine Learning Model 2: Linear Regression Model with Oversampled training data

* Accuracy: A balanced accuracy score of 0.99 (99%) suggests that 99% of the anticipated values are accurate.
* Precision: For a label of 0, the precision is 1, meaning that all healthy loans are accurately identified under label 0. This shows that the model is highly good at recognizing healthy loans. The precision for 1 label is 0.84 (84%) meaning that 84% of the values the model predicted as high-risk are accurate.
* Recall: For Label 1, the recall is 0.99 (99%), meaning that the model correctly identified 99% of the real high-risk loans (the support value for 1 label is 619) as such. Recall for label 0 is 0.99, meaning that 99% of the data are correctly labeled.
  

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
