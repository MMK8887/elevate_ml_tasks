# Customer Segmentation with K-Means Clustering

## 📄 Project Overview
This project performs **customer segmentation** using the **K-Means clustering** algorithm on a dataset containing demographic and spending behavior information. The goal is to group customers into distinct segments based on **Annual Income** and **Spending Score** to support targeted marketing strategies.

---

## 📊 Dataset Information
- **Number of records:** 200  
- **Number of columns:** 5  
- **Features:**
  - `CustomerID` — Unique identifier for each customer  
  - `Gender` — Male/Female  
  - `Age` — Customer’s age in years  
  - `Annual Income (k$)` — Annual income in thousands of dollars  
  - `Spending Score (1-100)` — Score assigned by the store based on customer spending habits  
- **Missing Values:** None  

---

## 🔍 Methodology
1. **Feature Selection:** Focused on `Annual Income (k$)` and `Spending Score (1-100)` for clustering.
2. **Optimal Cluster Selection:**  
   - Used **Elbow Method** to determine the optimal number of clusters.
   - Result: **5 clusters** was found to be suitable.
3. **Clustering:**  
   - Applied **K-Means clustering** with `n_clusters=5`.
4. **Evaluation:**  
   - Calculated **Silhouette Score** to assess cluster separation.  
     - Average Silhouette Score ≈ **0.554** (indicating reasonably good separation).
5. **Visualization:**  
   - Created a scatter plot of `Annual Income` vs. `Spending Score` showing 5 distinct clusters.

---

## 📈 Results
- Customers were successfully segmented into **5 distinct groups** based on spending habits and income.
- The clusters are visually well-separated, as confirmed by the scatter plot.
- **Silhouette Score** suggests that the clustering structure is meaningful and moderately strong.

---

## 🛠 Tools & Libraries
- **Python**
- **Pandas** — Data handling
- **Matplotlib / Seaborn** — Data visualization
- **Scikit-learn** — K-Means clustering & metrics

---

## 📌 Applications
- Targeted marketing campaigns.
- Personalized promotions.
- Customer loyalty program design.
- Identifying high-value customers.
