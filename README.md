# 🌿 Feature Selection and Model Evaluation on SMK_CAN_187 Dataset

## Project Summary
This project compares three feature selection methods — **Mutual Information (MI)**, **Recursive Feature Elimination (RFE)**, and **Lasso** — on the **SMK_CAN_187 dataset**.  
We evaluate **SVM** and **Random Forest (RF)** classifiers using **accuracy**, **F1 score**, **precision**, **recall**, and **AUC**, and use **SHAP** for model interpretability.

---

⭐ Overview

This project explores three major feature selection techniques — Mutual Information (MI), Recursive Feature Elimination (RFE), and Lasso — applied to the SMK_CAN_187 gene-expression dataset, a classic high-dimensional biomedical dataset.

After selecting features, two classifiers are trained:

Support Vector Machine (SVM)

Random Forest (RF)

Performance is evaluated using:

Accuracy

F1-Score

Precision

Recall

AUC

Finally, SHAP analysis is used to interpret which genes/features contribute most to model predictions.
---

🧭 Key Features

✔ Clean modular Python pipeline
✔ Three feature selection methods compared
✔ SVM & RF model training
✔ SHAP interpretability
✔ Ready-to-run Colab notebook
✔ Publication-style result tables
✔ Clear folder structure
✔ Easy reproducibility

---

---

⚡ GitHub Badges
![Python](https://img.shields.io/badge/Python-3.10-blue)
![Scikit-Learn](https://img.shields.io/badge/ScikitLearn-1.2+-yellow)
![Status](https://img.shields.io/badge/Project-Complete-green)
![SHAP](https://img.shields.io/badge/Explainability-SHAP-orange)

---
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

📁 Repository Folder Structure

Feature_Selection_Project_2025/
│
├── notebooks/                   # Colab notebook for experimentation
│   └── feature_selection.ipynb
│
├── src/                         # Python scripts for modular code
│   ├── config.py
│   ├── load_data.py
│   ├── feature_selection_mi.py
│   ├── feature_selection_rfe.py
│   ├── feature_selection_lasso.py
│   ├── train_models.py
│   └── shap_analysis.py
│
├── data/                        # Dataset or download instructions
│   └── README.md
│
├── results/                     # Model metrics and SHAP visualizations
│   ├── metrics.csv
│   └── shap_plots/
│       ├── svm_shap.png
│       └── rf_shap.png
│
├── requirements.txt             # Python dependencies
└── README.md                    # Main documentation


---

---

🔧 Installation & Setup

Clone the repo

git clone https://github.com/your-username/Feature_Selection_Project_2025.git
cd Feature_Selection_Project_2025

Create virtual environment (optional, recommended)

python -m venv venv
source venv/bin/activate      # macOS/Linux
venv\Scripts\activate         # Windows

Install dependencies

pip install -r requirements.txt

## 🚀 How to Run the Project

# Option 1 — Run the Notebook
# Option 2 — Run Python Scripts
---

## 🧩 Workflow Diagram

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
SHAP Interpretability
        │
        ▼
Results Saved (metrics.csv, shap_plots/)

---

---
📊 Results

📌 Full Results Table

| Feature Set             | Classifier | Accuracy | F1-Score | Precision | Recall | AUC  | Key Notes |
|-------------------------|-----------|----------|----------|-----------|--------|------|-----------|
| Full Dataset            | SVM       | 0.72     | 0.72     | 0.73      | 0.72   | 0.74 | Baseline performance limited by high dimensionality |
| Full Dataset            | RF        | 0.70     | 0.70     | 0.71      | 0.70   | 0.72 | RF sensitive to high feature-to-sample ratio |
| MI                      | SVM       | 0.77     | 0.77     | 0.78      | 0.77   | 0.80 | Best trade-off of performance vs. simplicity |
| MI                      | RF        | 0.77     | 0.77     | 0.78      | 0.76   | 0.81 | Stable performance; matches literature findings |
| RFE                     | SVM       | 0.98     | 0.98     | 0.99      | 0.98   | 0.99 | Extremely strong, but computationally expensive |
| RFE                     | RF        | 0.86     | 0.86     | 0.87      | 0.86   | 0.88 | Good improvement; less stable than SVM |
| LASSO                   | SVM       | 1.00     | 1.00     | 1.00      | 1.00   | 1.00 | Perfect sparsity & prediction |
| LASSO                   | RF        | 0.84     | 0.84     | 0.85      | 0.84   | 0.86 | Good dimensionality reduction but accuracy drops |
| Combined (MI + RFE + Lasso) | SVM   | 0.93     | 0.93     | 0.94      | 0.93   | 0.95 | Balanced hybrid selection; mitigates individual biases |
| Combined                | RF        | 0.79     | 0.79     | 0.80      | 0.79   | 0.82 | Stable but weaker vs SVM hybrid |

---

🔮 Future Improvements

Add PCA, Variance Threshold, and SelectKBest

Evaluate Gradient Boosting, XGBoost, and LightGBM

Hyperparameter tuning with GridSearchCV

Build an interactive SHAP dashboard

Integrate sklearn.pipeline for a full automated ML pipeline

Add cross-validation & statistical significance testing

---

🤝 Contributions

Contributions, pull requests, and suggestions are welcome.
