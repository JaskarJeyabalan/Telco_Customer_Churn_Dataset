# Telco Customer Churn Prediction – README

## 🔍 Project Overview

This project analyzes customer churn using the Telco Customer Churn dataset. It includes data cleaning, exploratory analysis, segmentation, predictive modeling, and business impact estimation. The goal is to identify churn drivers and recommend retention strategies.

## 📂 Dataset

- Source: Telco_Customer_Churn_Dataset (3).csv
- Rows: 7,043 | Columns: 21
- Target: Churn (Yes/No)

## 🧼 Data Preparation

- Stripped whitespace and handled missing values.
- Converted `TotalCharges` to float and imputed missing values with median.
- Created `TenureGroup` bins.
- Encoded categorical variables using Label Encoding and One-Hot Encoding.

## 📊 Exploratory Data Analysis

- Churn distribution by gender, senior citizen status, tenure, and charges.
- Boxplots and histograms for MonthlyCharges and TotalCharges.
- Churn rates segmented by contract type and payment method.

## 👥 Customer Segmentation

- Grouped customers by TenureGroup.
- Estimated monthly and total savings from retention efforts.
- Highlighted short-tenure customers (0–12 months) as high-risk churn group.

## 🤖 Churn Prediction Model

- Models: Logistic Regression, Decision Tree (GridSearchCV), Random Forest, Calibrated RF
- Scaled features where required.
- SHAP used for interpretability.

## 📈 Model Evaluation

- AUC, Accuracy, Precision, Recall, F1 Score
- Confusion matrix breakdown
- ROC and Precision-Recall curves
- Threshold analysis for decision optimization

## 💡 Business Recommendations

- Focus retention on short-tenure customers.
- Offer long-term contracts to reduce churn.
- Target high-charge customers with loyalty programs.
- Improve service quality for fiber/DSL users.

## 📊 Key Features

- Cleaned and encoded customer data
- Visualized churn patterns and savings potential
- Trained Logistic Regression, Decision Tree, Random Forest, and Calibrated RF
- Evaluated models using AUC, precision, recall, F1, and SHAP
- Estimated savings by tenure group and retention rate
- Created stakeholder-ready Excel dashboard

## 📁 File Structure

- Telco-Customer-Churn  (3).csv – Raw dataset
- churn_analysis.ipynb – Main notebook with full workflow
- Data_Preparation.ipynb – Modular script for cleaning and encoding
- Exploratory_Data_Analysis_(EDA).ipynb – Script for generating plots
- Customer_Segmentation.ipynb – Script for training and evaluating models
- Churn_Prediction_Model.ipynb – Script for Models and Shap
- Model_Evaluation.ipynb – Script for AUC, Accuracy, Precision, Recall, F1 Score, ROC and Precision-Recall curves
- Business_Recommendationsipynb – Script for Recommendations
- outputs/ – Contains plots and model reports

## 📦 Outputs

- Excel dashboard: `dashboard_summary.xlsx`
- Model summary, confusion matrix, threshold analysis
- Savings summary, SHAP and performance charts
- Business recommendations

## 🧑 Author

**Prepared by**: Jaskar Jeyabalan S
