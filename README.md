# Breast-Cancer-Diagnosis-Performance-Benchmarking-and-Statistical-Validation
Performance Benchmarking and Statistical Validation

This repository presents a comprehensive benchmarking and statistical validation of multiple machine learning models for breast cancer diagnosis using the Wisconsin Diagnostic Breast Cancer (WDBC) dataset.

The project emphasizes methodological rigor, statistical equivalence, and clinical relevance, rather than relying solely on peak accuracy.

📌 Project Overview

Evaluates 11 state-of-the-art machine learning models

Uses stratified 10-fold cross-validation

Applies non-parametric statistical tests (Friedman & Wilcoxon)

Reports clinically meaningful metrics

Demonstrates performance equivalence among top models

This work aligns with best practices in medical machine learning research.

📊 Dataset

Name: Wisconsin Diagnostic Breast Cancer (WDBC)

Source: UCI Machine Learning Repository (via sklearn)

Samples: 569

Features: 30 real-valued cytological features

Classes:

0 → Benign

1 → Malignant (positive class)

The dataset reflects realistic clinical class imbalance.

⚙️ Methodology
Preprocessing

Z-score normalization using StandardScaler

No feature selection (prevents data leakage)

Stratified data splitting

Validation Strategy

Stratified 10-fold cross-validation

Independent hold-out test set (20%)

🤖 Machine Learning Models
Support Vector Machines

SVM (RBF kernel)

SVM (Linear kernel)

Logistic Regression

L1-regularized

L2-regularized

Neural Network

Deep MLP (256–128–64–32)

Ensemble and Boosting Models

Random Forest

Extra Trees

Gradient Boosting

CatBoost

LightGBM

XGBoost

All models use optimized hyperparameters consistent with the project report.

📈 Evaluation Metrics

Accuracy

Precision

Recall (Sensitivity)

F1-score

ROC–AUC

Clinical Metrics

Specificity

False Positive Rate (FPR)

False Negative Rate (FNR)

📐 Statistical Validation

Friedman test for global model comparison

Wilcoxon signed-rank tests for pairwise comparisons against the best-performing model

Key Result

No statistically significant performance differences were observed among top-performing models at α = 0.05.

🧪 Key Results

Best Mean Accuracy:
SVM (RBF) → ~97.7% ± 1.6%

Independent Test Set Performance:

Accuracy ≈ 96.5%

Specificity ≈ 98.6%

Sensitivity ≈ 92.9%

These results highlight clinically relevant trade-offs between false positives and false negatives.

📊 Visualizations

The project includes:

Cross-validation performance distributions

ROC curves for all models

Confusion matrix for the best-performing model

Stability analysis across folds
