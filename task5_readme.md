# 🧠 Heart Disease Prediction - Model Evaluation Summary

This project explores machine learning models to predict heart disease using a variety of clinical features. Two key models—**Decision Tree** and **Random Forest** classifiers—were trained and evaluated for performance.

---

## 📊 Summary

### 🔍 Data Analysis Key Findings

- 🧪 **Initial Decision Tree**  
  - **Training Accuracy:** 1.0000 (100%)  
  - **Test Accuracy:** 0.9650 (96.5%)  
  - ➡️ Indicates **overfitting**, as the model performs perfectly on training data but less so on unseen data.

- 🌳 **Pruned Decision Tree (max_depth=3)**  
  - **Training Accuracy:** 0.8581  
  - **Test Accuracy:** 0.7899  
  - ✅ Smaller gap between training and test accuracy shows **reduced overfitting** at the cost of some accuracy.

- 🌲 **Random Forest Classifier**  
  - **Test Accuracy:** 0.9883 (98.83%)  
  - 🔝 Outperformed both full and pruned Decision Trees.

- 📌 **Feature Importance (Random Forest)**  
  - Most important features:
    - `oldpeak`
    - `thalach`
    - `thal_2`
    - `thal_3`
  - Least important features:
    - `restecg_2`
    - `ca_4`

- 🔁 **5-Fold Cross-Validation Results**  
  - **Mean Accuracy:** 0.9883  
  - **Standard Deviation:** 0.0110  
  - ✅ Both models demonstrated **robust and stable** performance estimates.

---

## ✅ Conclusion

- The **Random Forest model** is the best performing classifier in this analysis, achieving high accuracy and reliable generalization.
- **Feature importance insights** help in understanding model decisions and may guide future feature selection or data collection efforts.
- Cross-validation confirms the **stability** and **reliability** of model performance.

---
