# credit-risk-classification


## Overview of the Analysis

The scope of this project was to build a machine learning model to predict loan classifications based on the data provided in the 'lending_data.csv' file. 

The financial information in the dataset consisted of various features related to loan applicants, their financial history, and creditworthiness. Some of the more relevant features included income, debt-to-income ratio, employment length, and credit score, among others. The target variable to predict was the loan_status, which had two classes: 0 (healthy loan) and 1 (high-risk loan).

Before beginning the machine learning process, the distribution of the loan_status variable was examined using value_counts. This allowed an understanding of the the class imbalance issue in the dataset, where healthy loans significantly outnumbered high-risk loans.

To address the imbalance in the class, a resampling method known as RandomOverSampler was utilized from the imbalanced-learn library. This created a balanced dataset by oversampling the high risk loans.

The stages of the machine learning process included:

Data Preprocessing: From a Jupyter notebook, the CSV file 'lending_data.csv; was read and separated the features (X) and the target variable (y). The data was then split into training and testing datasets using train_test_split to evaluate the model's performance on unseen data.

Model Selection and Training: The method of logistic regression was used as our machine learning model. The LogisticRegression model was used from the sklearn.linear_model module and trained it using the resampled training data.

Model Evaluation: After training the logistic regression model, predictions were made on the testing data (X_test) and evaluated the model's performance using various metrics such as balanced accuracy, confusion matrix, and classification report. These metrics provided insights into the model's ability to predict both healthy loans and high-risk loans.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Balanced Accuracy Score: 0.9521



* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.