# Credit Risk Prediction using Machine Learning

![Python](https://img.shields.io/badge/Python-3.8%2B-blue) ![Pandas](https://img.shields.io/badge/Pandas-1.3%2B-green) ![NumPy](https://img.shields.io/badge/NumPy-1.21%2B-lightblue) ![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.0%2B-orange)
## 📌 Project Overview

This project is part of the **DevelopersHub Data Science Internship - Task 2**.  
The goal is to predict whether a loan applicant is likely to default (not fully pay) using machine learning techniques.

**Key steps:**
- Exploratory Data Analysis (EDA)
- Data cleaning & feature engineering
- Handling imbalanced data
- Logistic Regression model
- Model evaluation

## 📂 Dataset

- Source: Loan Prediction / Credit Risk Dataset  
- **Target variable:** `not_fully_paid`  
  - `0` → Loan fully paid  
  - `1` → Loan not fully paid (default risk)

## 🛠️ Technologies Used

| Library | Purpose |
|---------|---------|
| Pandas, NumPy | Data manipulation |
| Matplotlib, Seaborn | Visualization |
| Scikit-learn | Model building, preprocessing, evaluation |

## 📁 Repository Structure
.
├── credit_risk.ipynb # Jupyter notebook with full code
├── loan_data.csv # Dataset file
├── requirements.txt # Dependencies
└── README.md # This file

text

## 📊 Exploratory Data Analysis (EDA)

Performed the following visualizations and analyses:

- Dataset overview & info
- Missing value analysis
- Correlation heatmap
- Distribution plots (histograms)
- Boxplots (outlier detection)
- Target variable distribution

**Key insights:**
- Higher interest rates → higher default risk
- Lower FICO scores → higher default risk
- Dataset is **highly imbalanced** (more fully-paid loans)

## 🧹 Data Preprocessing

- Checked and handled missing values
- Handled outliers
- Renamed columns for readability
- One-Hot Encoding for categorical variables
- Feature scaling using `StandardScaler`

## ⚙ Feature Engineering

Created new features to improve model performance:

- `risk_score`
- `utilization_fico_ratio`
- `income_installment_ratio`

Also performed feature selection using correlation analysis.

## ⚖ Handling Imbalanced Data

The dataset had significantly more non-default cases than defaults.

**Solution applied:**
- Random undersampling
- Balanced classes before training

This improved the model's ability to detect risky borrowers.

## 🤖 Machine Learning Model

**Model used:** Logistic Regression

**Training steps:**
1. Train-test split
2. Feature scaling
3. Model training
4. Prediction
5. Evaluation

## 📈 Model Evaluation

| Metric | Description |
|--------|-------------|
| Accuracy | Overall correctness |
| Precision | Accuracy of positive predictions |
| Recall | Ability to find all defaulters |
| F1-score | Harmonic mean of precision & recall |
| Confusion Matrix | Visualizes TP, TN, FP, FN |

**Final results:**
- Balanced class prediction achieved
- Improved recall for detecting loan defaults
- Better minority class detection after handling imbalance

## 📷 Visualizations Included

- Correlation heatmap
- Count plots (target variable)
- Histograms of features
- Boxplots for outlier detection
- Confusion matrix

## 🧠 Learning Outcomes

Through this project, I learned:

- Complete data cleaning workflow
- Exploratory data analysis techniques
- Feature engineering for financial data
- Handling imbalanced datasets (undersampling)
- Logistic Regression for binary classification
- Model evaluation metrics for imbalanced problems
- Feature selection using correlation

## 🚀 Future Improvements

Possible enhancements:

- Random Forest Classifier
- SMOTE (Synthetic Minority Oversampling)
- Hyperparameter tuning (GridSearchCV)
- ROC-AUC analysis
- Deploy model using Flask or Streamlit

## 📌 Conclusion

A **Credit Risk Prediction** model was successfully developed using Logistic Regression. After preprocessing, feature engineering, and balancing the dataset, the model achieved balanced performance in identifying both default and non-default loan applicants. This project demonstrates the complete workflow of a real-world binary classification problem in finance.

## 👨‍💻 Author

**Mudassir Khan**  
Data Science Intern @ DevelopersHub  
Passionate about Data Science, AI, and Machine Learning

---

⭐ If you find this useful, please give it a star!
