# 🧬 Breast Cancer Diagnosis - Logistic Regression Analysis

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
- Standardized features using `StandardScaler`.

## 🤖 Model: Logistic Regression
- Trained on the standardized dataset, evaluated with default threshold (0.5).

### 📊 Evaluation Metrics (Test Set)
- **Confusion Matrix:** `[[70 1], [2 41]]`
- **Precision:** `0.9762`
- **Recall:** `0.9535`
- **ROC-AUC Score:** `0.9974`

## 📈 Probability Mapping
- Explained the **sigmoid function** for probability mapping.
- Enables flexible classification by adjusting the decision threshold.

## 🎯 Threshold Tuning
- Recall remains high until ~0.5 threshold, then drops significantly.
- Default 0.5 threshold provides optimal precision-recall balance.

## ✅ Conclusion
- Logistic Regression performs extremely well.
- Default threshold effective, but tuning is beneficial for high-stakes use cases.
