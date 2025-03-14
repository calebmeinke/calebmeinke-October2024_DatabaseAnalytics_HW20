# calebmeinke-October2024_DatabaseAnalytics_HW20

# Module 20 Report

## Overview of the Analysis

The purpose of this analysis is to develop a machine learning model that accurately predicts the creditworthiness of borrowers at a peer-to-peer lending services company. The financial data analyzed included information on the borrower's financial history, the individual loans tied to each borrower, and the loan details (amount, interest rate, and status). Using these factors, the dataset provided a binary loan status for each loan, denoted as healthy loans (0) and high-risk loans (1). This analysis sought to build a machine learning model that leverages the borrower and loan data to accurately predict the loan status as healthy or high-risk. This process included reading in the lending services company data, analyzing correlations between the various data categories, scaling the data for proper analysis, and generating a logistic regression analysis for the dataset. From there, assessment of a confusion matrix and a classification report provided the information needed to draw conclusions about the accuracy of the machine learning model. 

## Results

Due to exceptionally accurate results in the initial logistic regression model, this analysis did not pursue the use of other model types. Results from the logistic regression model provide justification for this outcome. The following classification report provides the data necessary to better understand the model performance and outcomes.


Classification Report:

              precision    recall  f1-score   support

           0       1.00      1.00      1.00     18759
           1       0.87      0.98      0.92       625

    accuracy                           0.99     19384
   macro avg       0.94      0.99      0.96     19384
weighted avg       1.00      0.99      0.99     19384

With 99% accuracy in loan risk prediction, this model performs extraordinarily well; however, this performance differs between the healthy loan (0) and high-risk loan (1) categories. In its analysis of healthy loans, the model is 100% precise at predicting healthy loans. Similarly, the model's recall correctly identifies 100% of the healthy loans, creating a perfect F-1 score between these metrics for this category. In contrast, the model's precision drops to 87% for high-risk loans, which indicates the model generates some false-negatives in its output, marking some high-risk loans as healthy loans. While the model's recall indicates the model is 98% accurate at identifying high-risk loans, the lower precision does introduce some risk if the model and its outputs are accepted. Generally, this model performs well, overall, but there is some room for revision and refinement. 

## Summary

Depending on the organization's risk tolerance, the performance of this model could be a cause for further revision. This effort would be focused on ensuring higher precision in identifying high-risk loans (reducing false negatives). Exploration of other models, including SVC, K-Nearest Neighbor, Decision Trees, Random Forests, Ada Boost, and others, may produce more accurate outputs for both the healthy and high-risk loan populations. Use of these models may sacrifice elements of complexity and detail, however, which could produce *less* favorable outcomes. Each model would need to be tested thoroughly to determine the best performing model. That stated, the logistic regression model's overall performance is effective, and model tuning could further improve the results for high-risk loan assessment. Given the already prodigious model results, this tuning approach is likely the best approach to take if further modification is required.
