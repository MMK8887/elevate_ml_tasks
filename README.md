# elevate_ml_tasks
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
