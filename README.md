# DA5401 A4: GMM-Based Synthetic Sampling for Imbalanced Data

<div align="center">
  <img src="https://img.shields.io/badge/Python-3.8+-blue.svg" alt="Python Version">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-orange.svg" alt="Jupyter">
  <img src="https://img.shields.io/badge/Status-Complete-green.svg" alt="Status">
</div>

## Student Information

| Field | Details |
|-------|---------|
| Name | Shivam Tiwari |
| Roll Number | DA25C019 |
| Course | DA5401 - Advanced Data Analytics |
| Assignment | Assignment 4: GMM-Based Synthetic Sampling for Imbalanced Data |
| Topic | GMM and Clustering-Based Sampling for Credit Card Fraud Detection |
| Submission Date | September 2025 |
| Notebook Cells | 40+ comprehensive cells with advanced methodology |

---

## Project Overview

This assignment addresses the challenge of fraud detection in highly imbalanced datasets using advanced synthetic sampling and clustering techniques. The project implements and compares three approaches for handling the extreme class imbalance in credit card transactions:

### Objective

Compare the performance of Logistic Regression classifiers trained on three different training sets:
1. Baseline: Original imbalanced data
2. GMM-only: Synthetic minority oversampling using Gaussian Mixture Model
3. GMM + CBU: Combined GMM-based oversampling and clustering-based undersampling

---

## Project Structure & Essential Files

```
Da5401-Assingment4-GMM-Sampling/
├── Assignment4_DA5401_final.ipynb    # Main Jupyter notebook
├── README.md                         # Project documentation
└── .gitignore                        # Git ignore rules
```

### Key Files for Evaluation

| Priority | File Name | Description | Assignment Relevance |
|----------|-----------|-------------|---------------------|
| Main | Assignment4_DA5401_final.ipynb | Main deliverable - advanced analysis | Assignment compliance |
| Dataset | creditcard.csv | Kaggle credit card fraud dataset (not included, see instructions) | Required dataset |
| Documentation | README.md | Project documentation | Professional presentation |
| PDF | DA5401 A4 GMM.pdf | Assignment report | Reference |

---

## Assignment Implementation: Analysis Pipeline

### Part A: Data Exploration and Baseline Model

- Loads and analyzes the creditcard.csv dataset (284,807 transactions)
- Examines class distribution and imbalance ratio (577:1)
- Trains baseline Logistic Regression on imbalanced data
- Evaluates using precision, recall, F1-score, and confusion matrix

### Part B: GMM-Based Synthetic Sampling

- Isolates minority class and applies feature scaling
- Uses Bayesian Information Criterion (BIC) to select optimal GMM components
- Fits GMM to minority class and generates synthetic samples
- Combines synthetic and original minority samples for balanced training

### Part C: Clustering-Based Undersampling (CBU)

- Applies KMeans clustering to majority class
- Uses elbow method to select optimal clusters
- Proportionally samples from each cluster to reduce majority class size
- Combines undersampled majority and augmented minority for final balanced dataset

### Part D: Model Training, Cross-Validation, and Evaluation

- Trains Logistic Regression on all three datasets
- Implements 5-fold stratified cross-validation for robust evaluation
- Performs statistical significance testing and calculates confidence intervals
- Compares models using precision, recall, F1-score, and ROC-AUC

---

## Key Findings & Results

### Performance Comparison: Minority Class Metrics

| Model      | Precision | Recall | F1-Score | ROC-AUC |
|------------|-----------|--------|----------|---------|
| Baseline   | 0.866     | 0.637  | 0.734    | 0.980   |
| GMM-only   | 0.985     | 0.943  | 0.964    | 0.984   |
| GMM + CBU  | 0.979     | 0.927  | 0.952    | 0.981   |

- GMM-based approaches significantly outperform baseline in recall and F1-score
- Cross-validation confirms results are robust and generalizable
- Combined GMM + CBU approach provides best balance between recall and model stability

---

## Technical Implementation Details

### Dataset Characteristics

| Attribute | Value | Impact |
|-----------|-------|--------|
| Total Transactions | 284,807 | Large-scale real-world dataset |
| Fraud Cases | 492 (0.17%) | Extreme class imbalance |
| Normal Cases | 284,315 (99.83%) | Majority class dominance |
| Features | 30 (V1-V28 PCA + Time + Amount) | Pre-processed for ML |
| Imbalance Ratio | 577:1 | Requires advanced sampling |

### Sampling and Modeling Strategy

- GMM-based synthetic sampling for minority class
- Clustering-based undersampling for majority class
- BIC optimization for GMM component selection
- KMeans clustering for majority class structure preservation
- Stratified cross-validation for robust model evaluation

---

## Getting Started

### Prerequisites & Environment Setup

```bash
# Python >= 3.8
# Jupyter Notebook >= 6.0

# Required Libraries
pandas >= 1.3.0
numpy >= 1.21.0
matplotlib >= 3.4.0
seaborn >= 0.11.0
scikit-learn >= 1.0.0
scipy >= 1.7.0
jupyter >= 1.0.0
notebook >= 6.4.0
nbconvert >= 6.0.0
```

### Quick Start Guide

1. Download `creditcard.csv` from Kaggle and place in project directory
2. Open `Assignment4_DA5401_final.ipynb` in Jupyter
3. Run all cells sequentially
4. Review outputs and analysis

### Installation Commands

```bash
pip install -r requirements.txt
jupyter notebook Assignment4_DA5401_final.ipynb
```

### Dataset Requirements

- File: `creditcard.csv` (download from Kaggle)
- Size: ~143 MB (not included in repo)
- Placement: Project root directory

---

## Assignment Compliance & Quality Assurance

| Part | Requirement | Implementation | Status |
|------|-------------|----------------|--------|
| Data Analysis | Load & analyze dataset | Complete | Yes |
| Baseline Model | Train & evaluate | Complete | Yes |
| GMM Sampling | Synthetic minority generation | Complete | Yes |
| Clustering | Majority class undersampling | Complete | Yes |
| Cross-Validation | Robust model evaluation | Complete | Yes |
| Statistical Analysis | Significance testing | Complete | Yes |
| Documentation | Professional comments & README | Complete | Yes |

---

## Conclusions & Academic Impact

- GMM-based synthetic sampling and clustering-based undersampling provide a robust solution for imbalanced fraud detection
- Cross-validation and statistical analysis confirm the reliability of results
- The combined approach is recommended for practical deployment in fraud detection systems

---

## Contact & Academic Information

Student: Shivam Tiwari  
Roll Number: DA25C019  
Course: DA5401 - Advanced Data Analytics  
Institution: Indian Institute of Technology Madras  
Assignment: A4 - GMM-Based Synthetic Sampling for Imbalanced Data

---

This notebook demonstrates advanced synthetic sampling and clustering techniques for imbalanced datasets, combining theoretical understanding with practical implementation and professional documentation.