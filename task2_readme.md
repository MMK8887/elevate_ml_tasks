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
