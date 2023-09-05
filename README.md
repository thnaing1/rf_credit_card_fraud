# Classification of Fraudulent Credit Card transactions using Random Forest

Dataset link: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

Introduction

Credit Card fraud is on the rise and is affecting every business and financial institution. We can deal with fraud using Machine Learning algorithms to correctly identify fraudulent transactions. 
Problem Statement
The problem of fraud detection is well suited to two-class classification. We intend to apply Random Forest to perform a classification task. My algorithm will take a dataset of credit card transactions and define them as fraud(1) or not fraud(0) using the various attributes in the dataset as factors in the training.

Dataset

For our dataset, we intend to use the “Credit Card Fraud Detection” dataset that is found on Kaggle. This dataset consists of anonymized credit card transactions labeled as fraudulent or genuine. The dataset comes from ULB Machine Learning Group which is a research unit of the Computer Science department at the Free University of Brussels. 
The table is in a typical CSV format. It has 284,808 rows and 31 attributes. It contains the columns time, amount, class, and factors V1-V28. It contains numerical input values that are the result of PCA(Principal Component Analysis) transformation. It does not contain original features due to the fact that credit card transactions are confidential. It is a highly imbalanced dataset. 
Methods
Due to the nature of the problem, the number of fraudulent transactions will be much lower than the number of legitimate ones. In other words, the dataset will be highly imbalanced. This is the primary reason why Random Forest was chosen.
Decision Trees are relatively robust to the outlier values. In addition, decision trees are more suited to problems that have complex decision boundaries like credit card fraud detection. 
Random Forest is able to aggregate the predictions of multiple decision trees which will reduce bias towards the majority class making it even more suitable for highly imbalanced datasets. In addition, Random Forest tends to have better generalization abilities due to its ensemble nature. 

Evaluation methods

For my evaluation metrics, I will be using both the F1 score. For our fraud detection algorithm, we want to have a high true positive rate meaning that our algorithm successfully detects when a true fraud case occurred. At the same time, we want to have a low false positive rate to prevent falsely detecting a case of fraud when there isn’t one. Using the precision and recall metrics allows us to successfully satisfy those requirements.
