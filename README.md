
# 🧠 Salary Prediction Machine Learning Project

Welcome to the **Salary Prediction** project where we built a complete machine learning pipeline — from raw CSV to production-ready prediction system.

---

## 📊 Dataset
- **Source**: [San Francisco Salaries Dataset – Kaggle](https://www.kaggle.com/code/pileatedperch/sf-salaries-exercise/input)
- **Description**: Contains salary data for San Francisco public employees, including base pay, overtime pay, total benefits, and job details.
- **Size**: ~150,000 records with multiple columns covering job classification, compensation, and employment year.

---

## 📌 Project Overview

This project predicts employee salaries using public job data and includes all end-to-end stages of a real ML workflow:

- Data Cleaning
- Feature Engineering
- Feature Selection
- Data Preprocessing
- Model Training
- Evaluation & Optimization
- Deployment & Prediction
- Interpretability

---

## 🗂️ Dataset Overview

The dataset includes job records with fields like:

- `BasePay`, `OvertimePay`, `OtherPay`, `Benefits`
- `TotalPay`, `TotalPayBenefits`
- `JobTitle`, `Status` (FT/PT), `Agency`

---

## 🛠️ Key Features Created

- `BasePlusOvertimePay`: Core salary (BasePay + OvertimePay)
- `TotalEarningsRatio`: TotalPay / BasePay
- `JobTitleEncoded`: Frequency encoding of job titles
- `Status_PT`: One-hot encoded employment type

---

## ✅ Modeling

- Used **Linear Regression** and **Random Forest**
- Applied **Min-Max Scaling** on features only
- Used **RandomizedSearchCV** for hyperparameter tuning
- Chose the best model based on:
  - Lower MSE & MAE
  - Higher R² Score (~0.76)

---

## 🎯 Deployment

- Saved the trained model: `salary_prediction_model.pkl`
- Saved the scaler: `scaler.pkl`
- Defined realistic employee inputs
- Pipeline accepts scaled inputs and predicts salary in dollars

---

## 📈 Example Prediction Output

| Employee | OtherPay | EarningsRatio | JobTitleEncoded | Status | Predicted Salary |
|----------|----------|----------------|------------------|--------|------------------|
| 1        | 0.2      | 0.009          | 0.2              | FT     | $41,392.43       |
| 2        | 0.7      | 0.0095         | 0.5              | FT     | $68,000.00+      |

---

## 📌 Tools & Libraries

- Python, Pandas, NumPy
- Scikit-learn, Seaborn, Matplotlib
- Joblib for model persistence

---

## ✅ Project Status: Completed

This project is **100% complete and production-ready**. It follows best practices for data science and machine learning workflows.

Feel free to test the model using the included `scaler.pkl` and `salary_prediction_model.pkl` with new employee feature vectors.

## 👏 Author
**Reza** — Full ML pipeline implemented from scratch.

## 📎 Credits
Dataset sourced from [Kaggle](https://www.kaggle.com/) for educational and research purposes. All rights to the original dataset belong to the respective uploader.
