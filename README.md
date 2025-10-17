# Missing Data Imputation Study: Credit Risk Assessment

## 📋 Project Overview

This project demonstrates and compares different strategies for handling missing data in the UCI Credit Card Default Clients Dataset. The study focuses on implementing and evaluating four imputation techniques to determine the most effective approach for credit risk prediction.

## 🎯 Objectives

1. **Artificially introduce** Missing At Random (MAR) values in key features
2. **Implement four imputation strategies**:
   - Strategy 1: Median Imputation (Baseline)
   - Strategy 2: Linear Regression Imputation
   - Strategy 3: Non-Linear Regression Imputation (KNN)
   - Strategy 4: Listwise Deletion
3. **Train and evaluate** Logistic Regression classifiers on each imputed dataset
4. **Compare performance** to determine the optimal missing data handling strategy

## 📊 Dataset

- **Source**: UCI Credit Card Default Clients Dataset
- **Records**: 30,000 credit card clients
- **Features**: 24 attributes including demographic information, credit history, and payment behavior
- **Target Variable**: `default.payment.next.month` (binary classification)

## 🔧 Missing Data Introduction

Artificially introduced Missing At Random (MAR) values in:
- **AGE**: 7% missing (2,100 records)
- **BILL_AMT1**: 8% missing (2,400 records)
- **BILL_AMT2**: 6% missing (1,800 records)

## 🛠️ Imputation Strategies

### 1. Median Imputation (Dataset A)
- **Approach**: Fill missing values with column medians
- **Rationale**: Robust to outliers, preserves distribution shape
- **Implementation**: Simple baseline method

### 2. Linear Regression Imputation (Dataset B)
- **Approach**: Predict missing AGE values using linear regression
- **Features**: All other columns except target variable
- **Assumption**: Missing At Random (MAR)

### 3. KNN Regression Imputation (Dataset C)
- **Approach**: Predict missing AGE values using K-Nearest Neighbors (k=5)
- **Advantage**: Captures non-linear relationships
- **Implementation**: Distance-weighted predictions

### 4. Listwise Deletion (Dataset D)
- **Approach**: Remove rows with any missing values
- **Result**: Reduced dataset size (5,860 records removed)

## 📈 Model Training & Evaluation

- **Algorithm**: Logistic Regression
- **Evaluation Metrics**:
  - Accuracy
  - Precision, Recall, F1-Score
  - Confusion Matrix
  - ROC-AUC Score

## 🚀 Key Findings

### Performance Comparison
- **Best Performing Strategy**: [To be determined after model evaluation]
- **Worst Performing Strategy**: [To be determined after model evaluation]
- **Key Insights**: [Summary of findings]

### Distribution Analysis
- Median imputation creates artificial spikes in distributions
- Regression-based methods preserve natural distribution patterns
- KNN captures more complex relationships than linear regression


