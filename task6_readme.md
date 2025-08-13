# KNN Classification on the Iris Dataset

## 📌 Overview
This project demonstrates the use of the **K-Nearest Neighbors (KNN)** algorithm for classifying the **Iris flower dataset**.  
The workflow covers data loading, preprocessing, exploratory analysis, model training, hyperparameter tuning, and evaluation.

---

## 📊 Dataset
The **Iris dataset** contains 150 samples with four numerical features:
- **Sepal Length**
- **Sepal Width**
- **Petal Length**
- **Petal Width**

Target variable:
- **Species** (`Iris-setosa`, `Iris-versicolor`, `Iris-virginica`)

---

## 🔍 Key Steps
1. **Data Preparation**
   - Loaded the dataset and separated **features** and **target variable**.
   - Normalized features to improve model performance.

2. **Train-Test Split**
   - Split data into **80% training** and **20% testing** sets.

3. **Model Training**
   - Trained a **KNN classifier** with various values of `K`.

4. **Evaluation**
   - Measured **accuracy** and analyzed **confusion matrices**.

5. **Hyperparameter Tuning**
   - Used **GridSearchCV** to find the best value of `K`.

6. **Visualization**
   - Created pairwise scatter plots to visualize class separability.

---

## 📈 Results

| **K Value** | **Test Accuracy** | **Misclassifications** |
|-------------|-------------------|------------------------|
| 1           | 0.967             | 1                      |
| 3           | 1.000             | 0                      |
| 5           | 1.000             | 0                      |
| 7           | 1.000             | 0                      |
| 9           | 1.000             | 0                      |

**Best Model:**
- `K = 3` (found via GridSearchCV)
- Cross-validation score: **0.9500**
- Test set accuracy: **1.0000**
- Perfect confusion matrix — no misclassifications.

---

## 📊 Insights from Visualization
- **Iris-setosa** is completely separable from the other two species based on all feature pairs.
- **Iris-versicolor** and **Iris-virginica** show slight overlap in **petal dimensions** but are still generally distinguishable.

---

## 🛠 Technologies Used
- **Python**
- **scikit-learn** (KNN, GridSearchCV)
- **pandas**, **numpy**
- **matplotlib**, **seaborn**

---

## 🚀 How to Run
```bash
# Clone this repository
git clone <repo_url>

# Install dependencies
pip install -r requirements.txt

# Run the script
python knn_iris.py
```

---

## 📌 Conclusion
The **KNN algorithm** performs exceptionally well on the Iris dataset, achieving **100% accuracy** for multiple values of `K`. Visualization confirms that the dataset is highly separable, especially for **Iris-setosa**.
