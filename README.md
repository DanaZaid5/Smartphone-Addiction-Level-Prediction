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

## 🔎 Key Takeaways & Limitations

The near-baseline accuracy (~25% for a 4-class problem) is itself a meaningful finding rather than a modeling failure. Several factors explain it:

- **Weak feature–target signal:** Feature importance and correlation analysis showed that no single feature—or combination of features—had a strong relationship with the self-reported addiction level. The available behavioral and demographic variables simply do not separate the four classes well.
- **Subjective, self-reported labels:** The target is based on users' *self-reported* addiction levels. Self-assessment is noisy and inconsistent between people, so two users with nearly identical usage patterns may report different levels—making the labels hard to predict from behavior alone.
- **Consistency across models:** Logistic Regression, Decision Tree, and Random Forest all converged to similar scores. When models of very different complexity plateau at the same point, the ceiling is usually in the data, not the algorithm.
- **Class overlap:** The confusion matrices showed heavy overlap between adjacent levels (e.g., Moderate vs. High), which is expected when the underlying classes are not clearly distinguishable.

**Conclusion:** Predicting subjective smartphone-addiction levels from these features is inherently difficult. Improving performance would likely require richer or more objective data (e.g., longer-term usage logs, validated psychological assessment scores, or physiological signals) rather than more complex models.

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
├── Smartphone_Addiction_with_live_demo.ipynb          # Full ML pipeline + live demo
├── Smartphone Addiction Level Prediction report.pdf   # Project report
├── SmartPhone addiction Level .pptx                   # Presentation slides
└── README.md
```

## 👥 Team

- Dana Alsalami
- Alya Almuqren
- Aljohara Alsultan
- Aljudy Altorkistani

