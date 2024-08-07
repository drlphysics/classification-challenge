# classification-challenge
## Overview
This project aims to classify emails as spam or legitimate using logistic regression and random forest models. The analysis involves splitting the data into training and testing sets, scaling the features, creating and evaluating the models. The objective is to determine which model performs better in classifying the emails.

## Repository Structure
spam-classification/
│
├── data/
│   ├── spam-data.csv
│
├── notebooks/
│   ├── spam_classification.ipynb
│
├── README.md
│
└── results/
    ├── logistic_regression_accuracy.txt
    ├── random_forest_accuracy.txt

## Instructions
### Step 1: Split the Data into Training and Testing Sets
Objective: Prepare the data for training and testing the models.

Read the data from the provided URL into a Pandas DataFrame.
In the notebook, make a prediction about which model you expect to perform better.
Create the labels set (y) from the “spam” column, and create the features (X) DataFrame from the remaining columns.
A value of 0 in the “spam” column means the message is legitimate.
A value of 1 means the message has been classified as spam.
Check the balance of the labels variable (y) using the value_counts function.
Split the data into training and testing datasets using train_test_split.
Output: Training and testing datasets.

### Step 2: Scale the Features
Objective: Normalize the feature data for better model performance.

Create an instance of StandardScaler.
Fit the StandardScaler with the training data.
Scale the training and testing features DataFrames using the transform function.
Output: Scaled training and testing features DataFrames.

### Step 3: Create a Logistic Regression Model
Objective: Train and evaluate a logistic regression model.

Fit a logistic regression model using the scaled training data (X_train_scaled and y_train). Set the random_state argument to 1.
Save the predictions on the testing data labels using the testing feature data (X_test_scaled) and the fitted model.
Evaluate the model’s performance by calculating the accuracy score of the model.
Output: Accuracy score of the logistic regression model.

### Step 4: Create a Random Forest Model
Objective: Train and evaluate a random forest classifier model.

Fit a random forest classifier model using the scaled training data (X_train_scaled and y_train).
Save the predictions on the testing data labels using the testing feature data (X_test_scaled) and the fitted model.
Evaluate the model’s performance by calculating the accuracy score of the model.
Output: Accuracy score of the random forest model.

### Step 5: Evaluate the Models
Objective: Compare the performance of the two models.

In the appropriate markdown cell, answer the following questions:
Which model performed better?
How does that compare to your prediction?
Output: Evaluation and comparison of model performance.