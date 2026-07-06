# 📱 Smartphone Addiction Level Prediction

A machine learning project that predicts smartphone addiction levels using behavioral and demographic data. The project compares multiple classification models and evaluates their ability to classify users into four addiction levels: **Low, Moderate, High, and Severe**.

## 📌 Overview

This project explores whether smartphone usage patterns and demographic information can be used to predict self-reported smartphone addiction levels. A complete machine learning pipeline was implemented, including data preprocessing, feature engineering, model training, hyperparameter tuning, and performance evaluation.

## 🎯 Objectives

- Predict smartphone addiction levels using supervised machine learning.
- Compare the performance of multiple classification algorithms.
- Analyze feature importance and feature-target relationships.
- Evaluate the impact of dataset quality on model performance.

## 📊 Dataset

- **Source:** Global Mobile Phone Addiction Dataset (Kaggle)
- **Samples:** 3,000 users
- **Features:** 34 behavioral and demographic features
- **Target:** Self_Reported_Addiction_Level

Example features include:
- Daily screen time
- Phone unlocks per day
- Social media usage hours
- Sleep hours
- Stress level
- Monthly data usage
- Age
- Gender
- Education level

## ⚙️ Data Preprocessing

- Removed unnecessary columns
- Corrected invalid negative values
- Handled missing values
- One-Hot Encoding for categorical variables
- Standardized numerical features
- Created engineered features:
  - `total_app_hours`
  - `usage_diversity`
  - `screen_to_sleep_ratio`

## 🤖 Machine Learning Models

- Logistic Regression
- Decision Tree
- Random Forest

Hyperparameter tuning was performed using **RandomizedSearchCV** with **5-fold Stratified Cross Validation**.

## 📈 Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix

## 📊 Results

| Model | Test Accuracy |
|--------|--------------:|
| Logistic Regression | 26.3% |
| Decision Tree | 25.2% |
| Random Forest | **27.0%** |

Although Random Forest achieved the highest accuracy, all models performed close to the random baseline (~25%), indicating weak relationships between the available features and the target labels.

## 🛠️ Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- SciPy
- Google Colab

## 📂 Repository Structure

```
├── Smartphone_Addiction_Final_with_live_demo.ipynb
├── Smartphone_Addiction_Report.pdf
├── README.md
└── dataset/
```

## 👥 Team

- Dana Alsalami
- Alya Almuqren
- Aljohara Alsultan
- Aljudy Altorkistani

