# Telecom Customer Churn Prediction - Indian Market

## Overview
This project explores customer churn in India's fast-evolving telecom sector. Using customer demographics and usage data from four major telecom providers (Airtel, Reliance Jio, Vodafone, BSNL), we aim to predict churn using machine learning models and uncover factors influencing customer retention.

## Datasets
Two CSV files were used:
1. **telecom_demographics.csv**
   - Customer demographics: age, gender, state, city, dependents, estimated salary, registration date, etc.
2. **telecom_usage.csv**
   - Usage patterns: number of calls made, SMS sent, data consumed, churn status.

## Analysis & Modeling
1. **Data Merging**: Merged demographics and usage data on `customer_id`.
2. **Data Preprocessing**:
   - One-hot encoded categorical variables (e.g., gender, city, telecom partner).
   - Feature scaling with `StandardScaler`.
3. **Model Training**:
   - Logistic Regression
   - Random Forest Classifier
4. **Evaluation**:
   - Compared model performance using confusion matrix and classification report.
   - Random Forest outperformed logistic regression in accuracy and F1-score.

## Key Insights
- Churn prediction is feasible using usage and demographic data.
- City, registration date, and data usage were influential features.
- Feature engineering on `registration_event` (like registration month) can further improve results.

## Tools & Libraries
- Python (pandas, scikit-learn)

## Results
Class Imbalance: 80% of customers did not churn, and only 20% did. This imbalance significantly affects recall for the churn class.
Logistic Regression:
   - Accuracy: 72%
   - Precision (Churn): 21%, Recall (Churn): 11%
   - Performs decently on non-churn predictions but struggles with actual churners.
Random Forest:
   - Accuracy: 79%
   - Precision (Churn): 0%, Recall (Churn): 0%
   - Heavily biased toward predicting non-churn due to class imbalance.

