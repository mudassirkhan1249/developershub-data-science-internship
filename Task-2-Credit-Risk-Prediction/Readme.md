# Credit Risk Prediction using Machine Learning

## 📌 Project Overview
This project focuses on predicting whether a loan applicant is likely to default on a loan using Machine Learning techniques. The goal is to analyze borrower information and classify applicants as either likely to fully repay the loan or not.

The project includes:
- Exploratory Data Analysis (EDA)
- Data Cleaning
- Feature Engineering
- Handling Imbalanced Data
- Logistic Regression Model
- Model Evaluation

---

# 📂 Dataset
Dataset used:
- Loan Prediction / Credit Risk Dataset

Target Variable:
- `not_fully_paid`

Meaning:
- `0` → Loan fully paid
- `1` → Loan not fully paid (default risk)

---

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

# 📊 Exploratory Data Analysis (EDA)

Performed:
- Dataset overview
- Missing value analysis
- Correlation heatmap
- Distribution plots
- Boxplots
- Target variable analysis

Key insights:
- Higher interest rates were associated with higher default risk.
- Lower FICO scores showed higher chances of default.
- Dataset was highly imbalanced.

---

# 🧹 Data Preprocessing

Steps performed:
- Checked missing values
- Handled outliers
- Renamed columns for better readability
- One-Hot Encoding for categorical variables
- Feature Scaling using `StandardScaler`

---

# ⚙ Feature Engineering

New features were created to improve model learning:

- `risk_score`
- `utilization_fico_ratio`
- `income_installment_ratio`

Feature selection was also performed using correlation analysis.

---

# ⚖ Handling Imbalanced Data

The dataset contained a significantly higher number of non-default cases compared to default cases.

To solve this issue:
- Random undersampling was applied
- Classes were balanced before training

This improved the model’s ability to detect risky borrowers.

---

# 🤖 Machine Learning Model

Model Used:
- Logistic Regression

Training Steps:
1. Train-Test Split
2. Feature Scaling
3. Model Training
4. Prediction
5. Evaluation

---

# 📈 Model Evaluation

Evaluation metrics used:
- Accuracy Score
- Precision
- Recall
- F1-score
- Confusion Matrix

Final Results:
- Balanced class prediction achieved
- Improved recall for detecting loan defaults
- Better minority class detection after handling imbalance

---

# 📷 Visualizations

The project includes:
- Correlation Heatmap
- Count Plots
- Histograms
- Boxplots
- Confusion Matrix

---

# 📚 Learning Outcomes

Through this project, the following concepts were learned:
- Data Cleaning
- EDA
- Feature Engineering
- Handling Imbalanced Datasets
- Logistic Regression
- Model Evaluation
- Feature Selection

---

# 🚀 Future Improvements

Possible future enhancements:
- Random Forest Classifier
- SMOTE for imbalance handling
- Hyperparameter Tuning
- ROC-AUC Analysis
- Model Deployment using Flask or Streamlit

---

# 📌 Conclusion

A Credit Risk Prediction model was successfully developed using Machine Learning techniques. After preprocessing, feature engineering, and balancing the dataset, the Logistic Regression model achieved balanced performance in identifying both default and non-default loan applicants.

This project demonstrates the complete workflow of a real-world binary classification problem in finance.

---

# 👨‍💻 Author

Mudassir Khan

Passionate about:
- Data Science
- Artificial Intelligence
- Machine Learning
- Problem Solving
