# Final Project Proposal

## 1. Certificate Name

**Maryan Mohamed Adam**

---

# 2. Project Title and Description

## Project Title

**AI-Powered Personal Wellness Recommendation System Using Machine Learning**

## Application Name

**WellMind AI**

## Description

WellMind AI is an AI-powered personal wellness recommendation system that uses machine learning to analyze lifestyle and health-related behaviors and provide personalized recommendations.

Many people experience problems such as poor sleep quality, high stress levels, low physical activity, and unhealthy daily habits without understanding their impact on overall wellness. This project aims to solve this problem by using machine learning techniques to analyze user information and generate personalized wellness recommendations.

The system considers factors such as sleep patterns, stress levels, physical activity, occupation, caffeine intake, water consumption, screen time, and lifestyle behaviors. Based on these factors, WellMind AI predicts the user's wellness category and provides recommendations such as improving sleep habits, increasing physical activity, managing stress, and maintaining healthy routines.

The target users are students, employees, and individuals who want to understand their lifestyle patterns and improve their daily wellness using artificial intelligence.

---

# 3. Problem Type

This project uses both supervised and unsupervised machine learning approaches.

## Supervised Learning (Classification)

The main problem type is classification.

The model will predict the user's wellness category:

- Healthy Lifestyle
- Average Lifestyle
- Poor Lifestyle

The prediction will be used to generate personalized recommendations.

## Unsupervised Learning (Clustering)

K-Means clustering will be used to discover hidden lifestyle patterns among users.

The system will identify groups such as:

- Healthy Lifestyle Users
- Sleep-Deprived Users
- High Stress Users
- Low Activity Users

---

# 4. Dataset

## Dataset Source

Kaggle:

[Sleep and Lifestyle Health Dataset](Kaggle Dataset Link)

## Dataset Size

The dataset contains more than **2,000 rows**, which is suitable for machine learning training, testing, and clustering analysis.

## Target Column

The target column will be:

**Lifestyle Category**

The target represents the overall wellness condition of the user:

- Healthy
- Average
- Poor

This target will be created through feature engineering based on sleep, stress, physical activity, and lifestyle factors.

---

# Main Features

| Feature | Description |
|---|---|
| Age | User age |
| Gender | User gender |
| Occupation | User work type |
| Sleep Duration | Number of sleeping hours |
| Sleep Quality | Quality of sleep |
| Physical Activity Level | Daily activity level |
| Stress Level | Stress intensity |
| BMI Category | Body weight category |
| Daily Steps | Number of daily steps |
| Screen Time | Daily device usage time |
| Water Intake | Daily water consumption |
| Caffeine Intake | Daily caffeine consumption |
| Time of Day | Morning, Afternoon, Evening, Night |

---

# 5. Feature Engineering

New features will be created to improve machine learning performance.

## Sleep Score

Calculates sleep quality based on:

- Sleep Duration
- Sleep Quality

## Fatigue Score

Measures tiredness using:

- Sleep Score
- Stress Level
- Physical Activity

## Activity Score

Measures physical activity using:

- Daily Steps
- Physical Activity Level

## Stress Index

Converts stress levels into numerical values for machine learning.

## Caffeine Balance

Analyzes caffeine consumption and its relationship with sleep and stress.

## Wellness Score

Combines:

- Sleep Score
- Activity Score
- Stress Index
- Hydration Level
- Lifestyle factors

## Productivity Index

Measures productivity based on:

- Sleep
- Stress
- Activity Level

## Lifestyle Category

Generated classes:

- Healthy
- Average
- Poor

---

# 6. Algorithms You Plan to Train

## 1. Logistic Regression

Used as a baseline classification model because it is simple, interpretable, and suitable for multi-class prediction.

## 2. Decision Tree

Used because it can learn non-linear patterns and provide understandable decision rules.

## 3. Random Forest

Used because it combines multiple decision trees and improves prediction accuracy while reducing overfitting.

## 4. XGBoost

Used because it is a powerful boosting algorithm that performs well on structured datasets.

## 5. K-Means Clustering

Used for unsupervised learning to identify different lifestyle groups without predefined labels.

---

# 7. Evaluation Plan

## Classification Metrics

The classification models will be evaluated using:

- Accuracy
- Precision
- Recall
- Macro F1 Score
- Confusion Matrix

## Clustering Metrics

The clustering models will be evaluated using:

- Silhouette Score
- Davies-Bouldin Index

## Best Model Selection

The best classification model will be selected using **Macro F1 Score** because it provides balanced performance across all wellness categories.

For clustering, the best model will be selected using the highest **Silhouette Score**.

---

# 8. Deployment Sketch

The backend will be developed using **FastAPI**.

## API Endpoint

## Input Example

```json
{
  "age": 25,
  "gender": "Female",
  "sleep_hours": 5,
  "sleep_quality": 6,
  "stress_level": "High",
  "activity_level": "Low",
  "daily_steps": 3000,
  "caffeine_intake": 2,
  "water_intake": 1000
}
Output Example
{
  "prediction": "Poor Lifestyle",
  "wellness_score": 55,
  "recommendations": [
    "Improve sleep duration",
    "Increase physical activity",
    "Reduce stress"
  ],
  "confidence": 0.91
}
# 9. Repository Plan
wellmind-ai/

├── dataset/
│   ├── raw/
│   └── processed/

├── notebooks/
│   ├── 01_eda.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_model_training.ipynb
│   └── 05_clustering.ipynb

├── src/
│   ├── preprocess.py
│   ├── feature_engineering.py
│   ├── train.py
│   └── evaluate.py

├── models/
│   └── best_model.pkl

├── api/
│   └── app.py

├── frontend/

├── README.md

└── requirements.txt


# Expected Outcome

The final system will provide users with personalized wellness recommendations using machine learning techniques. The system will analyze lifestyle factors such as sleep patterns, stress levels, physical activity, caffeine intake, hydration, and daily habits to predict the user's wellness category and generate suitable recommendations.

The project will compare multiple machine learning models to identify the best-performing model for wellness prediction. Additionally, clustering techniques will be used to discover hidden lifestyle patterns and group users based on similar wellness behaviors.

The WellMind AI application will present predictions, wellness scores, user lifestyle groups, and personalized recommendations through an interactive dashboard. This system aims to help users better understand their daily habits, improve their lifestyle choices, and make informed wellness decisions using artificial intelligence.