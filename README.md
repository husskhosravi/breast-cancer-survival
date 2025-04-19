# 🧬 Breast Cancer Survival Prediction

## Overview
This project focuses on predicting breast cancer survival outcomes using machine learning. We combine data exploration, data cleaning, feature engineering, class imbalance handling (SMOTE), and model selection/tuning (Random Forest, among others) to achieve reliable predictive performance.

## 📁 Dataset Overview

The dataset includes patient-level data such as:

- **Demographics**: Age, Gender
- **Biomarkers**: Protein expression levels (Protein1–4)
- **Clinical Info**: Tumour stage, Histology, Hormone receptor status (ER, PR, HER2)
- **Surgical Data**: Type of surgery performed
- **Outcome**: `Patient_Status` → _Alive_ or _Dead_

---

## 🧠 Project Objective

> Predict whether a breast cancer patient will survive based on their clinical and molecular features.

---

## 📊 ML Pipeline

## 1. Data Exploration 🔎
- **Objective**: Understand the dataset structure and identify key features (e.g., gender, tumour stage, histology, receptor statuses).
- **Tools & Methods**:  
  - **pandas** for data loading and inspection (e.g., `head()`, `info()`).  
  - **seaborn** and **matplotlib** for exploratory visualisations (bar charts, etc.).  
- **Outcome**: Gained insights into class distribution, identified missing values, and confirmed the presence of categorical variables requiring encoding.

---

## 2. Data Cleaning 🧹
- **Objective**: Ensure data quality by removing or correcting invalid entries.
- **Steps**:  
  - Dropped rows containing null values.  
  - Standardised or renamed certain columns to maintain consistency (e.g., tumour stage).
- **Outcome**: A refined dataset, free of empty or inconsistent rows, ready for further processing.

---

## 3. Feature Engineering ⚙️
- **Objective**: Convert categorical variables into numeric representations suitable for machine learning models.
- **Methods**:  
  - **Mapping** tumour stages (I, II, III) and histology types into numeric codes.  
  - **Encoding** receptor statuses (ER, PR, HER2) and surgery types into integers.
- **Outcome**: A fully numeric feature matrix, preserving the essential information from categorical fields.

---

## 4. Train-Test Split 🔀
- **Objective**: Evaluate model performance by holding out a portion of the data.
- **Methods**:  
  - Used **scikit-learn**’s `train_test_split` to split data into training (90%) and test (10%) sets.
- **Outcome**: Two subsets: one for training models and tuning parameters, and one for unbiased performance evaluation.

---

## 5. Model Training 🤖
- **Objective**: Build and optimise machine learning models to predict survival status.
- **Approach**:
  1. **Class Imbalance Handling**: Applied **SMOTE** (Synthetic Minority Over-sampling Technique) to oversample the minority class in the training set.  
  2. **Random Forest**: Performed a **GridSearchCV** to optimise hyperparameters (e.g., `n_estimators`, `max_depth`, `class_weight`).  
- **Outcome**: A best-fit Random Forest model with tuned parameters, ready for evaluation.

---

## 6. Model Evaluation 📊
- **Objective**: Assess how well the final model predicts patient survival.
- **Tools & Metrics**:
  - **accuracy** to gauge overall correctness.
  - **classification_report** (precision, recall, F1-score) to measure class-specific performance.
  - **confusion_matrix** to understand true positives/negatives vs. false positives/negatives.
- **Outcome**: Quantified performance of the model on unseen test data. Identified areas for further improvement, especially regarding minority-class predictions.

---

## Technologies & Libraries Used
- **Python** (core language)
- **pandas**, **numpy** (data manipulation)
- **seaborn**, **matplotlib** (visualisation)
- **scikit-learn** (machine learning algorithms, model evaluation)
- **imblearn** (SMOTE for class imbalance)

--

**Thank you for checking out this project!**  
