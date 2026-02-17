# 🏦 Beta Bank Customer Churn Prediction

## 📌 Project Overview
This project focuses on predicting customer churn for **Beta Bank**. Since acquiring new customers is significantly more expensive than retaining current ones, the goal is to identify clients at risk of leaving the bank.

Using historical behavior data, I developed a classification model that prioritizes the **F1-score** to balance precision and recall, ensuring that we catch as many potential churns as possible without losing accuracy on loyal customers.

---

## 📊 Key Findings & Insights

The project successfully identified the best approach to predict customer churn, exceeding the required F1-score of 0.59.

### Model Performance Comparison
| Approach | F1-Score | AUC-ROC |
| :--- | :---: | :---: |
| **Baseline (Random Forest)** | 0.5785 | **0.8554** |
| **Class Weight Balanced (Optimized)** | **0.6000** | 0.8482 |
| **Random Undersampling** | 0.5877 | 0.8544 |

> **Success:** The Optimized Class Weight approach achieved an **F1-score of 0.60**, surpassing the target threshold.

### Strategic Insights
* **Top Churn Drivers:** Feature importance analysis revealed that **Age**, **Estimated Salary**, and **Credit Score** are the most critical factors influencing a customer's decision to leave.
* **Class Imbalance:** Standard models failed to identify churners effectively. Applying **Class Weight Balancing** proved superior to Undersampling, providing the best trade-off for the bank's needs.
* **Business Opportunity:** The model is highly accurate at identifying loyal customers (low False Positives). However, the remaining False Negatives suggest room for a more aggressive retention strategy for customers flagged as high-risk.

---

## 🧪 Technical Highlights
* **Advanced Imputation:** Used **KNN Imputer** ($k=5$) to handle missing values in the `Tenure` column, preserving data distribution better than simple mean/median filling.
* **Feature Engineering:** * Dropped non-informative features (`RowNumber`, `CustomerId`, `Surname`).
    * Applied **One-Hot Encoding** to categorical variables (`Geography`, `Gender`).
* **Imbalance Handling:** Compared three strategies: Baseline, Manual Undersampling, and Class Weight Balancing.
* **Feature Importance:** Analysis revealed that **Age**, **Estimated Salary**, and **Credit Score** are the primary drivers of customer churn.

---

## 📂 Project Structure
```text
BETA-BANK-CHURN-PREDICTION/
├── dataset/
│   └── Churn.csv
├── notebook/
│   └── notebook.ipynb
├── .gitignore
├── environment.yml
└── README.md
```

---

## 🛠️ Tech Stack
* **Python 3.10**
* **Pandas & NumPy** — Data cleaning and transformation.
* **Scikit-Learn** — Machine Learning pipeline (KNN Imputer, Random Forest).
* **Matplotlib & Seaborn** — Visual insights and Confusion Matrix.

---

🚀 How to Run
Clone the repository.

* Create the environment: conda env create -f environment.yml.

* Activate it: conda activate beta-bank-env.

* Run the notebook in notebook/notebook.ipynb.

---

👤 Autor
Pedro Albuquerque 
Data Science | Data Analyst | Business Intelligence

---

## 🤝 Contact
[![LinkedIn](https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/phaa/)
