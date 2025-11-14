# Feature Selection and Model Evaluation on SMK_CAN_187 Dataset

## Project Summary
This project compares three feature selection methods — **Mutual Information (MI)**, **Recursive Feature Elimination (RFE)**, and **Lasso** — on the **SMK_CAN_187 dataset**.  
We evaluate **SVM** and **Random Forest** classifiers using **accuracy** and **F1 score**, and use **SHAP** for model interpretability.

1. Repo Folder Structure
Feature_Selection_Project_2025/
│
├── notebooks/
│   └── feature_selection.ipynb
│
├── src/
│   ├── config.py
│   ├── load_data.py
│   ├── feature_selection_mi.py
│   ├── feature_selection_rfe.py
│   ├── feature_selection_lasso.py
│   ├── train_models.py
│   └── shap_analysis.py
│
├── data/
│   └── README.md        # Instructions on obtaining the dataset
│
├── results/
│   ├── metrics.csv
│   └── shap_plots/
│       ├── svm_shap.png
│       └── rf_shap.png
│
├── requirements.txt
└── README.md


2. GitHub Repository Description

Title: Feature Selection and Model Evaluation on SMK_CAN_187 Dataset

Description: A comparison of Mutual Information, RFE, and Lasso feature selection methods on the SMK_CAN_187 dataset, with SVM and Random Forest classifiers. Includes model evaluation, SHAP interpretability, and results visualization.

Topics/Tags: Machine Learning, Feature Selection, SVM, Random Forest, SHAP, Python, Data Science, MSc Project

Feature_Selection_Project_2025/
│
├── notebooks/ # Colab notebook for experimentation
├── src/ # Python scripts for modular code
├── data/ # Dataset or download instructions
├── results/ # Metrics and SHAP plots
├── requirements.txt # Python dependencies
└── README.md



---

## Workflow Diagram

```text
Raw Data (SMK_CAN_187)
        │
        ▼
Data Loading (load_data.py)
        │
        ▼
Feature Selection
    ├── Mutual Information
    ├── RFE
    └── Lasso
        │
        ▼
Model Training (SVM, Random Forest)
        │
        ▼
Evaluation (Accuracy, F1)
        │
        ▼
SHAP Interpretability & Plots
        │
        ▼
Results Saved (metrics.csv, shap_plots/)


Future Improvements

Experiment with more feature selection methods (e.g., PCA, SelectKBest with different scoring)

Test additional models: Gradient Boosting, XGBoost, or Neural Networks

Hyperparameter tuning for both SVM and RF using GridSearchCV

Create an interactive SHAP dashboard for better visualization

Integrate automated pipeline with sklearn.pipeline for reproducibility
