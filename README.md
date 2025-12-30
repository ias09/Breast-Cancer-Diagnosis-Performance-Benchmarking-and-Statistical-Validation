# Breast-Cancer-Diagnosis-Performance-Benchmarking-and-Statistical-Validation
📌 Overview

This project presents a comprehensive comparative analysis of machine learning models for breast cancer diagnosis using the Wisconsin Diagnostic Breast Cancer (WDBC) dataset.

Unlike many studies that focus solely on peak accuracy, this work emphasizes:

Rigorous cross-validation

Statistical significance testing

Performance stability

Clinically meaningful evaluation metrics

The project benchmarks 11 state-of-the-art machine learning classifiers and demonstrates that several models achieve statistically equivalent performance, highlighting the importance of robustness and clinical context over marginal accuracy gains.

📊 Dataset

Name: Wisconsin Diagnostic Breast Cancer (WDBC)

Source: UCI Machine Learning Repository (via sklearn)

Samples: 569

Features: 30 real-valued cytological features

Target Classes:

0 → Benign

1 → Malignant (positive class)

The dataset reflects realistic clinical class imbalance (≈63% benign, 37% malignant).

⚙️ Methodology
🔹 Preprocessing

Z-score normalization using StandardScaler

No feature selection (avoids data leakage)

Stratified splitting to preserve class distribution

🔹 Models Evaluated (11)

Support Vector Machines

SVM (RBF kernel)

SVM (Linear kernel)

Logistic Regression

L1-regularized

L2-regularized

Neural Network

Deep MLP (256–128–64–32)

Ensemble & Boosting Methods

Random Forest

Extra Trees

Gradient Boosting

CatBoost

LightGBM

XGBoost

🔹 Evaluation Framework

Stratified 10-fold Cross-Validation

Metrics:

Accuracy

Precision

Recall (Sensitivity)

F1-score

ROC–AUC

Statistical Testing

Friedman test (global comparison)

Wilcoxon signed-rank test (pairwise comparison vs best model)

🔹 Test Set Evaluation

Independent hold-out test set (20%)

Confusion matrix

Clinically relevant metrics:

Sensitivity

Specificity

False Positive Rate

False Negative Rate

🧪 Key Findings

Best Mean Accuracy:
SVM (RBF) → 97.7% ± 1.6%

Statistical Result:
Friedman test shows no statistically significant difference among top-performing models (p > 0.05)

Clinical Insight:
Multiple models are viable for deployment; selection should consider:

Interpretability

Stability

Risk tolerance (false positives vs false negatives)

📈 Visualizations

The project includes:

Cross-validation performance distributions

ROC curves for all models

Confusion matrix for best model

Stability analysis across folds
