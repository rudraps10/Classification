# 🩺 Diabetes Prediction using Machine Learning

This project focuses on predicting diabetes using the Pima Indians Diabetes Dataset. It walks through an end-to-end machine learning pipeline: from data cleaning and EDA to training and evaluating multiple models.

---

## 📌 Problem Statement

Predict whether a person has diabetes (1) or not (0) using various medical and personal attributes like glucose level, insulin, BMI, blood pressure, etc.

---

## 📂 Dataset Info

- **Source**: Pima Indians Diabetes Dataset (Kaggle/UCI)
- **Rows**: 768
- **Target Column**: `Outcome` (0 = Non-diabetic, 1 = Diabetic)

---

## 🧹 Data Preprocessing

- Replaced biologically invalid zeros in: `Glucose`, `BloodPressure`, `BMI`, `Insulin`, and `SkinThickness` with column-wise mean
- Imputation was done separately on training and test sets to avoid data leakage
- Handled outliers using **IQR capping**
- Scaled features using `StandardScaler`

---

## 📊 Exploratory Data Analysis (EDA)

- **Distribution plots** and **boxplots** for each feature
- **Correlation heatmap** to show relationships between variables
- **Pairplots** for selected important features
- **Outcome-wise boxplots** for: `Glucose`, `BMI`, `Age`, `BloodPressure`
- **Countplot** for `Outcome` distribution

---

## 🤖 Models Tried

| Model                | Accuracy |
|---------------------|----------|
| K-Nearest Neighbors | ~78%     |
| Logistic Regression | ~75%     |
| Random Forest       | ~75%     |

All models evaluated using:
- Accuracy score
- Confusion matrix
- Classification report

---

## 🧠 Key Insights

- Data cleaning had a huge impact on accuracy
- `Insulin` and `SkinThickness` had ~45% missing values, requiring smart imputation
- Random Forest performed well with minimal tuning
- Feature scaling was necessary for KNN and Logistic Regression
- Visual EDA helped understand the feature distributions and class separability

---

## 🛠️ Libraries Used

- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `scikit-learn`

---

## ✅ Final Thoughts

This was an excellent hands-on project to practice:

- Data cleaning
- Model comparison
- Evaluation metrics
- Visualization

Further improvement possible by:
- Trying XGBoost or LightGBM
- Feature engineering
- Hyperparameter tuning

---
