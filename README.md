# **Fraud Detection in Credit Card Transactions**

## Project Overview

This project focuses on detecting fraudulent credit card transactions using a variety of machine learning algorithms. The workflow includes data ingestion, exploratory analysis, preprocessing, model training, evaluation, and deployment. Key steps include:

- Loading and understanding the "creditcard.csv" dataset.
- Visualizing data distributions and understanding inter-feature relationships through EDA.
- Standardizing features and preparing train-test splits while maintaining class balance.
- Training multiple models (Logistic Regression, Random Forest, XGBoost, and LightGBM) and comparing their performance using evaluation metrics such as F1-scores and AUC-ROC.
- Creating visual performance summaries including histograms, confusion matrix, and precision-recall/ROC curves.
- Saving the best performing model (LightGBM) for future deployment.

This comprehensive approach ensures transparency and reproducibility throughout the detection pipeline.


## Dataset
Loaded the "creditcard.csv" dataset containing transaction records with features such as Time, Amount, and various anonymized variables (V1 to V28) along with the target variable (Class).

## Project Steps

### 1. Exploratory Data Analysis (EDA):

- Visualized class distribution using histograms.  
- Examined feature distributions with subplots and histograms.  
- Computed and visualized the correlation matrix as a heatmap.

### 2. Data Preprocessing:

- Dropped unnecessary columns (Time, Amount, Class) for certain analyses.  
- Applied standard scaling to the features with `StandardScaler`.  
- Prepared train-test splits maintaining class balance with stratification.

### 3. Model Training & Evaluation:
- Built and evaluated multiple models:
    - Logistic Regression  
    - Random Forest (with balanced class weights)  
    - XGBoost (with adjusted scale_pos_weight)  
    - LightGBM (with optimized class weight and a custom probability threshold)
- Evaluated models using classification reports, F1-scores, and AUC-ROC scores.
- Generated performance visualizations including a bar plot comparing F1-scores, confusion matrix heatmap, and Precision-Recall & ROC curves.

### 4. Model Deployment:

- The best performing model (LightGBM) was saved using `joblib` for later deployment or further evaluation.

Overall, the workflow moves from data loading and visualization through preprocessing, diverse model training, thorough evaluation, and finally model storage, ensuring each step is transparent and reproducible.