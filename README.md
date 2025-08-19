# 📊 Telco Customer Churn Analysis & Prediction

## 🧠 Overview
This project analyzes customer churn behavior using the Telco dataset and builds predictive models to identify at-risk customers. It also estimates potential savings from retention efforts and provides actionable business recommendations.

## 📁 Dataset
- **Source**: `Telco_Customer_Churn_Dataset (3).csv`
- **Records**: 7,043 customers
- **Features**: 21 columns including demographics, service usage, contract details, and churn status

## 🔧 Project Workflow

### 1. Data Preparation
- Cleaned whitespace, handled missing values, and converted `TotalCharges` to float
- Imputed missing values with median
- Removed duplicates and standardized formats

### 2. Feature Engineering
- Created `TenureGroup` bins
- Label encoded binary features
- One-hot encoded categorical variables
- Added `EstimatedSavings` based on Monthly and Total Charges

### 3. Exploratory Data Analysis (EDA)
- Visualized churn distribution across:
  - Gender, SeniorCitizen status
  - Tenure, MonthlyCharges, TotalCharges
  - Contract type and PaymentMethod

### 4. Customer Segmentation
- Grouped churn rates by `TenureGroup`
- Estimated potential savings from retention
- Built savings summary tables and visualizations

### 5. Churn Prediction Models
- Models used:
  - Logistic Regression
  - Decision Tree (GridSearchCV)
  - Random Forest
  - Calibrated Random Forest
- Scaled features where needed

### 6. Model Evaluation
- Metrics: Accuracy, Precision, Recall, F1 Score, AUC
- Confusion Matrix breakdown
- ROC and Precision-Recall curves
- Threshold analysis for decision optimization

### 7. SHAP Interpretability
- Used SHAP to explain feature importance
- Generated summary plots for top contributing features

### 8. Business Recommendations
- Focus retention on short-tenure customers (0–12 months)
- Offer long-term contracts to reduce churn
- Target high-paying customers with loyalty programs
- Improve service quality for fiber/DSL users

## 📦 Outputs
| File | Description |
|------|-------------|
| `model_comparison.xlsx` | Model metrics summary |
| `confusion_breakdown.xlsx` | Confusion matrix details |
| `threshold_analysis.xlsx` | Threshold performance |
| `combined_savings_summary.xlsx` | Retention savings estimates |
| `dashboard_summary.xlsx` | Consolidated Excel dashboard with charts and recommendations |

## 📈 Visuals
- ROC Curve Comparison
- Precision-Recall Curve
- SHAP Summary Plot
- Savings by Tenure Group
- Model Performance Bar Chart

## 🧩 Dependencies
```bash
pandas
numpy
matplotlib
seaborn
shap
scikit-learn
openpyxl
