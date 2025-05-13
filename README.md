# Customer Churn Prediction Analysis
This project provides an end-to-end solution for predicting customer churn using machine learning. It includes data exploration, preprocessing, feature engineering, model training, evaluation, and business recommendations.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Features](#features)
- [Usage](#usage)
- [Methodology](#methodology)
- [Business Recommendations](#business-recommendations)

## Project Overview

Customer churn prediction helps businesses identify customers who are likely to stop using their services. This project:

- Analyzes customer data to understand churn patterns
- Builds machine learning models to predict churn probability
- Provides actionable business insights to reduce churn
- Offers a reusable pipeline for churn prediction

## Dataset

The analysis uses the IBM Telco Customer Churn dataset which includes:

- 7,043 customer records
- 20 features including:
  - Demographic info (gender, senior citizen status)
  - Account information (tenure, contract type)
  - Services subscribed (phone, internet, streaming)
  - Charges (monthly, total)
  - Churn status (target variable)

For your own dataset, replace the data loading section in the notebook.

## Features

Key features of this project:

1. **Data Preprocessing**:
   - Handling missing values
   - Feature type conversion
   - Target variable encoding

2. **Exploratory Data Analysis**:
   - Univariate and bivariate analysis
   - Correlation analysis
   - Churn rate visualization

3. **Feature Engineering**:
   - Creating tenure groups
   - Calculating average monthly charges
   - One-hot encoding categorical features

4. **Modeling**:
   - Logistic Regression (baseline)
   - Random Forest (with hyperparameter tuning)
   - Gradient Boosting (with hyperparameter tuning)
   - SMOTE for handling class imbalance

5. **Evaluation**:
   - Multiple metrics (Accuracy, Precision, Recall, F1, ROC AUC)
   - Confusion matrices
   - Feature importance analysis

## To USE
# Load your new data
new_data = pd.read_csv('new_customers.csv')

# Make predictions
predictions = predict_churn(new_data)

# View results
predictions[['customerID', 'Churn_Probability', 'Churn_Prediction']]

## Methodology

1. **Data Preparation**:
Cleaned and preprocessed raw data
Handled class imbalance using SMOTE

2. **Model Development**:
Implemented multiple classification algorithms
Performed hyperparameter tuning using GridSearchCV

3. **Evaluation**:
Used stratified train-test split (80-20)
Evaluated models using multiple metrics

Selected best model based on F1 score

## Business Recommendations

# Based on the analysis, we recommend:

**Targeted Retention**:
Focus on month-to-month contract customers
Create special offers for electronic check users

**Service Improvements**:
Bundle security features with internet service
Improve tech support for high-risk customers

**Proactive Measures**:
Implement early warning system using the model
Develop loyalty programs for long-tenure customers
