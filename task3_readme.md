# 🏡 Housing Price Prediction - Data Analysis Summary

## 📊 Overview
This project involves analyzing a housing dataset to build predictive models for estimating property prices. The goal was to understand the influence of various features on housing prices and assess the performance of linear regression models.

## 🔍 Key Findings

### Missing Data:
- The dataset had **no missing values**.

### Data Preprocessing:
- Binary categorical variables were converted to numerical values (0 or 1).
- The `furnishingstatus` column was one-hot encoded, generating new binary columns: `semi-furnished` and `unfurnished`.

### Data Splitting:
- The dataset was split into training (80%) and testing (20%) subsets.

## 📈 Model Performance

### 1. Simple Linear Regression
- **Feature Used:** `area`
- **Test R²:** 0.27
- **MAE:** $1,474,748.13
- **MSE:** $3,675,286,604,768.19
- **Interpretation:** Explains ~27% of the variance in price using only the `area` feature.

### 2. Multiple Linear Regression
- **Features Used:** All preprocessed features
- **Test R²:** 0.65
- **MAE:** $970,043.40
- **MSE:** $1,754,318,687,330.66
- **Interpretation:** Explains ~65% of the variance in housing prices.

## 💡 Feature Insights (from Model Coefficients)
- **Bathrooms:** A one-unit increase in the number of bathrooms is associated with a price increase of approximately $1.09 million.
- **Unfurnished Status:** Properties marked as unfurnished tend to have prices approximately $413,000 lower than the baseline furnishing category.
