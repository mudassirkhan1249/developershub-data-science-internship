# 🏦 Customer Churn Prediction (Bank Customers)

## 📌 Project Overview
This project focuses on predicting customer churn for a banking institution using the **Churn Modelling Dataset**. The primary objective is to identify customers who are likely to leave the bank (`Exited = 1`) so that the bank can take proactive retention measures. 

By applying systematic data preprocessing, feature engineering, and evaluating feature correlations, the final classification model achieves an **Overall Accuracy of 82%** and a **Recall of 60%** for predicting churned customers.

---

## 🛠️ Key Skills & Concepts Applied
* **Exploratory Data Analysis (EDA)** & Data Cleaning
* **Categorical Data Encoding** (One-Hot Encoding via `pd.get_dummies`)
* **Feature Engineering** (Creating high-impact custom behavior metrics)
* **Handling Multicollinearity** (Correlation Heatmap analysis to drop redundant features)
* **Class Imbalance Management** (SMOTE - Synthetic Minority Over-sampling Technique)
* **Supervised Classification Modeling** (Random Forest Classifier)
* **Feature Importance Evaluation**

---

## 🚀 Workflow & Implementation Steps

### 1. Data Preprocessing & Cleaning
* Handled missing and redundant rows.
* Encoded categorical features:
  * `Gender` converted to a numeric binary column `is_Female` ($0$ for Male, $1$ for Female).
  * `Geography` transformed using One-Hot Encoding with `drop_first=True` to prevent the dummy variable trap.

### 2. Feature Engineering
Created advanced behavioral features to improve model signal density:
* `ProductsPerYear`: `NumOfProducts` divided by `Tenure` (captures product adoption speed).
* `BalanceToSalaryRatio`: Account balance relative to estimated salary.

### 3. Correlation Matrix & Feature Selection
Analyzed the **Correlation Heatmap** to identify and resolve high multicollinearity:
* **Dropped `Tenure`** due to its high negative correlation ($-0.69$) with `ProductsPerYear`.
* **Dropped `HighRiskActive`** due to its high negative correlation ($-0.59$) with `Balance`.
* Kept strong predictors like `Age`, `IsActiveMember`, and `Geography_Germany`.

### 4. Handling Class Imbalance
The original target variable (`Exited`) was heavily skewed ($80\%$ stayed, $20\%$ left). To prevent model bias, **SMOTE** was applied *only on the training dataset* post-train-test split to ensure clean evaluation on a realistic test set.

### 5. Feature Scaling
Applied `StandardScaler` to normalize numeric ranges across features like `Age`, `Balance`, and `EstimatedSalary`.

---

## 📊 Model Performance

A **Random Forest Classifier** was trained on the resampled and scaled training data, producing the following optimal test results:

```text
--- Model Performance Report ---
Accuracy Score: 0.82

Classification Report:
              precision    recall  f1-score   support

           0       0.90      0.88      0.89      1593
           1       0.56      0.60      0.58       407

    accuracy                           0.82      2000
   macro avg       0.73      0.74      0.73      2000
weighted avg       0.83      0.82      0.83      2000
```

### 📈 Business Insights:
* **High Recall (60%):** The bank can successfully capture $60\%$ of all customers who intend to leave before they actually exit.
* **Balanced F1-Score (0.58):** Removing multicollinear features directly boosted the model's reliability, balancing false alarms against correct detections.

---

## 🔍 Top Features Influencing Churn

The model identified the following top factors driving customer exits:
1. **Age:** The absolute highest impact feature ($20.2\%$). Mature/senior customers show a significantly higher tendency to churn.
2. **NumOfProducts & ProductsPerYear:** Customer engagement stability is deeply tied to how many active accounts/services they hold over time.
3. **IsActiveMember:** Inactive membership serves as a direct, strong behavioral warning sign of an impending exit.

---

## 🛠️ How to Run This Project

1. Clone this repository:
   ```bash
   git clone https://github.com
   ```
2. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn
   ```
3. Execute the Python training script:
   ```bash
   python churn_prediction.py
   ```
