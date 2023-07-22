# credit-risk-classification


## Overview of the Analysis

The scope of this project was to build a machine learning model to predict loan classifications based on the data provided in the 'lending_data.csv' file provided by the bootcamp. 

The financial information in the dataset consisted of various features related to lending. The target variable to predict was the 'loan_status', which had two classes: 0 (healthy loan) and 1 (high-risk loan).

Before beginning the machine learning process, the distribution of the loan_status variable was examined using value_counts. This allowed an understanding of the the class imbalance issue in the dataset, where healthy loans significantly outnumbered high-risk loans. To address the imbalance in the class, the RandomOverSampler module was utilized from the imbalanced-learn library. This created a balanced dataset by oversampling the high risk loans.

The stages of the machine learning process included:

#### Data Preprocessing: 
From a Jupyter notebook, the CSV file 'lending_data.csv' was read and separated the features (x) and the target variable (y). The data was then split into training and testing datasets using train_test_split to evaluate the model's performance.

#### Model Selection and Training: 
The method of logistic regression was used as our machine learning model. The LogisticRegression model was used from the sklearn.linear_model module and trained it using the resampled training data.

#### Model Evaluation: 
After training the logistic regression model, predictions were made on the testing data (X_test) and evaluated the model's performance using various metrics such as balanced accuracy, confusion matrix, and classification report. These metrics provided insights into the model's ability to predict both healthy loans and high-risk loans.

## Results

### Machine Learning Model 1:

• Balanced Accuracy Score: 0.9521

• The balanced accuracy score for Model 1 is 0.9521352751368186, which indicates that the model achieved an average accuracy of 95.21% in predicting both healthy loans (class 0) and high-risk loans (class 1). This score considers the class imbalance and provides a fair assessment of the model's performance on both classes.

• Precision for Class 0 (Healthy Loan): 1.00
Model 1 achieved a precision of 1.00 (100%) for class 0, meaning that when it predicts a loan as a healthy loan, it is correct 100% of the time.

• Recall for Class 0 (Healthy Loan): 1.00
The recall for class 0 is 1.00 (100%), indicating that Model 1 correctly identifies all the healthy loans that are contained in the dataset. 

• Precision for Class 1 (High-Risk Loan): 0.86
Model 1 achieved a precision of 0.86 (86%) for class 1, meaning that when it predicts a loan as a high-risk loan, it is correct about 86% of the time. The model has a good ability to correctly identify high-risk loans.

• Recall for Class 1 (High-Risk Loan): 0.91
The recall for class 1 is 0.91 (91%), indicating that Model 1 correctly identifies approximately 91% of the actual high-risk loans in the dataset. 


### Machine Learning Model 2:

•Balanced Accuracy Score: 0.9942

•The balanced accuracy score for Model 2 is 0.9942, which indicates that the model achieved an average accuracy of 99.42% in predicting both healthy loans (class 0) and high-risk loans (class 1). This score provides a fair assessment of the model's performance on both classes.

•Precision for Class 0 (Healthy Loan): 1.00
Model 2 achieved a precision of 1.00 (100%) for class 0, indicating that when it predicts a loan as a healthy loan, it is correct 100% of the time. 

•Recall for Class 0 (Healthy Loan): 0.99
The recall for class 0 is 0.99 (99%), meaning that Model 2 correctly identifies approximately 99% of the actual healthy loans in the dataset. 

•Precision for Class 1 (High-Risk Loan): 0.85
Model 2 achieved a precision of 0.85 (85%) for class 1, indicating that when it predicts a loan as a high-risk loan, it is correct about 85% of the time. The model has a good ability to correctly identify high-risk loans.

•Recall for Class 1 (High-Risk Loan): 0.99
The recall for class 1 is 0.99 (99%), meaning that Model 2 correctly identifies approximately 99% of the actual high-risk loans in the dataset. The model has a low false negative rate for high-risk loans.

## Summary

In summary, for this analysis, two machine learning models were utilized to predict loan classifications. One was training on the original data, with the second being training after resampling

| Model 1 Metric                   | Model 1 Score | Model 2 Metric                   | Model 2 Score |
|--------------------------------- |-------------- |--------------------------------- |-------------- |
| Balanced Accuracy Score          | 0.9521        | Balanced Accuracy Score          | 0.9942        |
| Precision for Class 0 (Healthy Loan) | 1.00       | Precision for Class 0 (Healthy Loan) | 1.00       |
| Precision for Class 1 (High-Risk Loan) | 0.86    | Precision for Class 1 (High-Risk Loan) | 0.85    |
| Recall for Class 0 (Healthy Loan) | 1.00          | Recall for Class 0 (Healthy Loan) | 0.99          |
| Recall for Class 1 (High-Risk Loan) | 0.91       | Recall for Class 1 (High-Risk Loan) | 0.99       |


Model 2 is recommended as it seems to perform best and as it achieved higher balanced accuracy and recall for high-risk loans. Identifying high-risk loans accurately is extremely important for lending to avoid potential loss. However, this recommendation comes with a consideration of the importance of recall for high-risk loans and interpretability trade-offs. Therefore performance does depend on what problem is being solved.

