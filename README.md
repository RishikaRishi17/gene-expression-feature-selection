# Feature Selection and Model Evaluation on SMK_CAN_187 Dataset

## Project Summary
This project compares three feature selection methods — **Mutual Information (MI)**, **Recursive Feature Elimination (RFE)**, and **Lasso** — on the **SMK_CAN_187 dataset**.  
We evaluate **SVM** and **Random Forest (RF)** classifiers using **accuracy**, **F1 score**, **precision**, **recall**, and **AUC**, and use **SHAP** for model interpretability.

---

## Repository Folder Structure

Feature_Selection_Project_2025/
│
├── notebooks/ # Colab notebook for experimentation
│ └── feature_selection.ipynb
├── src/ # Python scripts for modular code
│ ├── config.py
│ ├── load_data.py
│ ├── feature_selection_mi.py
│ ├── feature_selection_rfe.py
│ ├── feature_selection_lasso.py
│ ├── train_models.py
│ └── shap_analysis.py
├── data/ # Dataset or download instructions
│ └── README.md
├── results/ # Metrics and SHAP plots
│ ├── metrics.csv
│ └── shap_plots/
│ ├── svm_shap.png
│ └── rf_shap.png
├── requirements.txt # Python dependencies
└── README.md


---

## GitHub Repository Description

**Title:** Feature Selection and Model Evaluation on SMK_CAN_187 Dataset  
**Description:** A comparison of Mutual Information, RFE, and Lasso feature selection methods on the SMK_CAN_187 dataset, with SVM and Random Forest classifiers. Includes model evaluation, SHAP interpretability, and results visualization.  
**Topics/Tags:** `Machine Learning`, `Feature Selection`, `SVM`, `Random Forest`, `SHAP`, `Python`, `Data Science`, `MSc Project`

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
Evaluation (Accuracy, F1, Precision, Recall, AUC)
        │
        ▼
SHAP Interpretability & Plots
        │
        ▼
Results Saved (metrics.csv, shap_plots/)
