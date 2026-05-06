# Customer Churn Prediction (Fintech)

## Overview

This project focuses on predicting customer churn in a banking environment using machine learning. The goal is to identify customers who are likely to leave, enabling proactive retention strategies and reducing revenue loss.

---

## Problem Statement

Customer churn is a critical issue in the fintech industry. Retaining existing customers is more cost-effective than acquiring new ones.
This project builds a predictive model to detect high-risk customers based on their financial behavior.

---

## Approach

### Data Preprocessing

- Removed irrelevant columns
- Handled missing values
- Converted categorical churn labels into binary format

### Feature Selection

Key financial behavior features:

- Customer Age
- Credit Limit
- Total Transaction Amount
- Total Transaction Count
- Total Revolving Balance
- Credit Utilization Ratio
- Months on Book
- Total Relationship Count

---

## Model Pipeline

1. Train-test split (with stratification)
2. Feature scaling using StandardScaler
3. Logistic Regression model training
4. Prediction using optimized decision threshold

---

## Model Optimization

- Applied **class balancing (`class_weight='balanced'`)**
- Adjusted **decision threshold (0.4)** to improve churn detection
- Focused on **recall over accuracy**, aligning with business needs

---

## Model Performance

- **Accuracy:** 80%
- **Churn Recall:** 82%
- **Churn Precision:** 44%

### Key Insight:

The model is optimized to **maximize recall**, ensuring most churn customers are identified, even at the cost of higher false positives.

---

## Evaluation Metrics

- Confusion Matrix
- Classification Report
- ROC-AUC Curve

---

## Feature Importance

Key drivers of churn:

- Low transaction count → higher churn risk
- Low customer engagement → higher churn
- High usage and activity → better retention

---

## Business Insights

- Customers with **low transaction frequency** are more likely to churn
- Customers with **fewer banking relationships** show higher churn probability
- Engagement is the strongest indicator of retention

---

## Business Impact

- Enables early identification of at-risk customers
- Supports targeted retention campaigns
- Helps reduce revenue loss due to churn

---

## Future Improvements

- Threshold tuning based on business cost
- Try advanced models (XGBoost, Random Forest)
- Deploy as a real-time prediction API

---

## Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib & Seaborn

---

## Conclusion

This project demonstrates how machine learning can be applied in fintech to solve real-world problems.
The focus was not only on building a model but also on aligning it with business objectives by prioritizing churn detection.
