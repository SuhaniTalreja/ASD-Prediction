# 🧠 ASD Prediction Using Machine Learning

This project focuses on building a machine learning model to predict the likelihood of Autism Spectrum Disorder (ASD) based on user input data. ASD is a developmental disorder that affects communication and behavior, and early detection can play a significant role in improving quality of life.

## 🚀 Project Overview

The goal is to develop an intelligent system that uses a machine learning model to assess an individual's ASD risk based on medical and behavioral traits. The system can assist healthcare professionals and caregivers in making early assessments.

## 📊 Dataset

The dataset used for training and testing was sourced from [Autism Screening Adult Dataset (UCI Repository)](https://archive.ics.uci.edu/ml/datasets/Autism+Screening+Adult). It contains various features including:

- A1–A10 (10 screening questions)
- Age
- Gender
- Ethnicity
- Jaundice at birth
- Family history of ASD
- Country of residence
- Used the screening app before
- Relation (Who filled the form)
- Result (ASD positive/negative)

---

## 🌟 Contribution

While ASD prediction through machine learning already exists, model accuracy and reliability can still be improved. This project implements a series of enhancements aimed at boosting prediction performance:

### 1. 📌 Data Preprocessing & Balancing

#### • Handling Outliers:
- Applied **Interquartile Range (IQR)** to detect outliers.
- Rather than removing them, outliers were replaced with the **median**, maintaining dataset size and structure while reducing skew.

#### • Handling Class Imbalance:
- Used **SMOTE (Synthetic Minority Oversampling Technique)** to create synthetic samples for the minority class instead of duplicating existing ones.
- This results in better model generalization and reduces bias toward the majority class.

#### • Label Encoding:
- Transformed non-numeric categorical variables into numerical form using **Label Encoding**, enabling efficient processing by ML algorithms.

---

### 2. 🧠 Feature Selection & Model Optimization

#### • Feature Selection with SelectKBest:
- Applied **SelectKBest** to retain only the most predictive features.
- This improves performance, prevents overfitting, and enhances model interpretability.

#### • Hyperparameter Tuning using RandomizedSearchCV:
- Used **RandomizedSearchCV** for tuning hyperparameters instead of exhaustive Grid Search.
- This reduces computational time while still achieving near-optimal parameters.

---

### 3. 🔁 Advanced Model Training & Stacking

#### • Trained Multiple Classifiers:
- **Decision Trees** – interpretable and useful for quick prototyping.
- **Random Forest** – ensemble method reducing overfitting and improving performance.
- **XGBoost** – optimized and scalable gradient boosting technique known for excellent performance on structured data.

#### • Ensemble via Stacking Classifier:
- Implemented a **stacking ensemble** where predictions from base models (Random Forest, XGBoost, Decision Trees) are used as features for a meta-classifier (e.g., Logistic Regression).
- The meta-classifier learns to combine model predictions optimally, leading to improved final accuracy.

---

## 🛠️ Technologies Used

- **Python**
- **Pandas**, **NumPy** – Data manipulation
- **Matplotlib**, **Seaborn** – Data visualization
- **Scikit-learn**, **XGBoost**, **Imbalanced-learn** – Machine learning & resampling
- **Jupyter Notebook** – Development



