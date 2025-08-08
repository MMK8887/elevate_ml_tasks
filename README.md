# elevate_ml_tasks
#task4
____
# 🧬 Breast Cancer Diagnosis - Logistic Regression Analysis

This project performs exploratory data analysis and classification on the Wisconsin Breast Cancer dataset using Logistic Regression. The primary objective is to predict whether a tumor is **malignant (M)** or **benign (B)** based on various features computed from digitized images of fine needle aspirate (FNA) of breast masses.

---

## 📁 Dataset Overview

- **Total Records:** 569
- **Initial Features:** 33
- **Target Variable:** `diagnosis` (M = Malignant, B = Benign)

### 🔧 Data Preprocessing

- Dropped:
  - `id` column (not relevant for analysis)
  - `Unnamed: 32` (contained only null values)
- Encoded `diagnosis`:
  - M → 1
  - B → 0
- Standardized features using `StandardScaler` to ensure all variables contribute equally to the model.

---

## 🤖 Model: Logistic Regression

The model was trained on the **standardized dataset**, and evaluated using the default threshold (0.5).

### 📊 Evaluation Metrics (Test Set)

- **Confusion Matrix:**  
  `[[70 1], [2 41]]`  
  - 70 True Negatives  
  - 1 False Positive  
  - 2 False Negatives  
  - 41 True Positives

- **Precision:** `0.9762`
- **Recall:** `0.9535`
- **ROC-AUC Score:** `0.9974`

---

## 📈 Probability Mapping

- Explained the **sigmoid function** used in Logistic Regression to map raw model output into a probability between 0 and 1.
- This probability enables flexible classification by adjusting the decision threshold.

---

## 🎯 Threshold Tuning

- Plotted **recall** vs various thresholds to evaluate model sensitivity.
- Observed that:
  - Recall remains **consistently high up to ~0.5**
  - Then **declines significantly** beyond that point
- The default threshold of **0.5** provided an optimal balance between precision and recall.

---

## ✅ Conclusion

- The Logistic Regression model performs **extremely well** on this dataset.
- The default threshold is effective, but analysis confirms threshold tuning can help in high-stakes environments where recall or precision may need to be prioritized.





#task3
___
🏡 Housing Price Prediction - Data Analysis Summary
📊 Overview
This project involves analyzing a housing dataset to build predictive models for estimating property prices. The goal was to understand the influence of various features on housing prices and assess the performance of linear regression models.

🔍 Key Findings
Missing Data:
The dataset had no missing values.

Data Preprocessing:

Binary categorical variables were converted to numerical values (0 or 1).

The furnishingstatus column was one-hot encoded, generating new binary columns: semi-furnished and unfurnished.

Data Splitting:

The dataset was split into training (80%) and testing (20%) subsets.

📈 Model Performance
1. Simple Linear Regression
Feature Used: area

Test R²: 0.27

MAE: $1,474,748.13

MSE: $3,675,286,604,768.19

Interpretation:
The model explains ~27% of the variance in price using only the area feature.

2. Multiple Linear Regression
Features Used: All preprocessed features

Test R²: 0.65

MAE: $970,043.40

MSE: $1,754,318,687,330.66

Interpretation:
Using all available features, the model explains ~65% of the variance in housing prices.

💡 Feature Insights (from Model Coefficients)
Bathrooms:
A one-unit increase in the number of bathrooms is associated with a price increase of approximately $1.09 million.

Unfurnished Status:
Properties marked as unfurnished tend to have prices approximately $413,000 lower than the baseline furnishing category.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------




#task1
# Titanic Dataset Preprocessing

## 📋 Overview

This project focuses on preprocessing the Titanic dataset to prepare it for further analysis or machine learning modeling. The following steps were taken to clean and transform the data:

---

## 🔍 Summary of Preprocessing Steps

### 1. 📉 Handling Missing Values
- **Age**: Missing values imputed using the **median** of the column.
- **Embarked**: Missing values filled using the **mode** (most frequent value).
- **Cabin**: Dropped due to a high proportion of missing values.

### 2. 🏷️ Categorical Feature Encoding
- All categorical features (excluding `'Name'`) were **one-hot encoded** to convert them into a numerical format suitable for ML models.

### 3. 🔢 Numerical Feature Scaling
- Numerical features (excluding `'PassengerId'`) were scaled using **StandardScaler** to ensure a mean of 0 and standard deviation of 1.

### 4. 📊 Outlier Detection and Treatment
- **Boxplots** revealed outliers in the following numerical columns: `'Age'`, `'SibSp'`, `'Parch'`, and `'Fare'`.
- Outliers were **capped at the 1st and 99th percentiles** to reduce their influence while retaining the data.

---

## 🧰 Tools Used

- **Python**
- **Pandas**
- **Scikit-learn**
- **Matplotlib / Seaborn** (for visualization)

---

## 📁 Output

The cleaned and transformed dataset is now ready for:
- Exploratory Data Analysis (EDA)
- Machine Learning modeling
- Visualization and insight generation

---
#task2 
# 🧊 Titanic Dataset – Exploratory Data Analysis (EDA) Summary

This document summarizes insights gained from the exploratory data analysis (EDA) of the Titanic dataset. The goal was to understand how different numerical features relate to passenger survival.

## 🔍 Key Insights by Feature

### 🎯 Survived
- **Summary**: Majority of passengers did **not survive**.
- **Statistics**: Mean is less than 0.5, with the boxplot skewed below 0.
- **Implication**: The dataset is imbalanced, with more non-survivors than survivors.

### 🛏️ Pclass (Passenger Class)
- **Distribution**: Most passengers belonged to **Pclass 3**, followed by Pclass 1 and 2.
- **Correlation**:
  - `Pclass` vs `Survived`: **-0.34** (negative correlation).
  - `Pclass` vs `Fare`: **-0.61** (strong negative).
- **Insight**: Passengers in **lower classes were less likely to survive**, and **paid lower fares**.

### 👶 Age
- **Distribution**: Roughly normal distribution with a peak near the median age.
- **Outliers**: Present, especially in older age groups.
- **Correlation**:
  - `Age` vs `Survived`: **-0.06** (very weak).
  - `Age` vs `SibSp`: **-0.27**, `Age` vs `Parch`: **-0.19**.
- **Insight**: Age alone is **not a strong predictor** of survival, but may interact with other variables.

### 👨‍👩‍👧 SibSp & Parch
- **Distribution**: Most passengers traveled with few or no family members.
- **Outliers**: Some passengers traveled with large families.
- **Correlation**:
  - `SibSp` vs `Survived`: **-0.02**
  - `Parch` vs `Survived`: **0.09**
  - `SibSp` vs `Parch`: **0.45**
- **Insight**: Weak individual correlation with survival, but **Parch** has a slightly stronger positive effect.

### 💸 Fare
- **Distribution**: Highly **right-skewed**, with many high-value outliers.
- **Correlation**:
  - `Fare` vs `Survived`: **0.27** (positive)
- **Insight**: Higher fare values are **associated with greater survival chances**, likely due to better cabins/class.

## 🧠 Overall Conclusion
- **Strongest predictors (numeric)**:  
  - **Pclass** (negative correlation)  
  - **Fare** (positive correlation)
- **Moderate influence**:  
  - **Parch**, **Age** (in context), **SibSp**
- **Outliers**: Present in Age, SibSp, Parch, and especially Fare — may require handling before modeling.

