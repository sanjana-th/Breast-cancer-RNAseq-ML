# Breast Cancer RNA-seq Classification
![Python](https://img.shields.io/badge/Python-3.10-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Classification-green)
![RNA-seq](https://img.shields.io/badge/Data-RNAseq-orange)

## Overview
This project implements supervised machine learning models to classify tumor vs normal breast tissue samples using bulk RNA-seq transcriptomic data (GSE58135).

## Dataset
- GEO Accession: GSE58135
- 168 total samples
- 28 breast cancer cell lines removed using metadata from series matrix
- Final dataset:
  - 84 Primary Tumor samples
  - 56 Normal breast tissue samples

## Data Preprocessing
1. Extracted sample metadata from GEO series matrix.
2. Removed breast cancer cell lines.
3. Filtered low-expression genes (counts ≥ 10 in ≥ 10 samples).
4. Log2 transformation of count data.
5. Standardization (Z-score scaling).
6. Dimensionality reduction using PCA (95% variance retained → 92 principal components).

## Model Training
Trained and compared three supervised machine learning models:
- Logistic Regression
- Linear Support Vector Machine (SVM)
- Random Forest

Stratified train-test split and 5-fold cross-validation were used for robust evaluation.

## Model Performance
- Logistic Regression Accuracy: 96%
- ROC-AUC: 0.98
- Strong separation between tumor and normal transcriptomic profiles.

## Visualization
Visualization performed using:
- matplotlib (ROC curves, PCA variance plot)
- seaborn (confusion matrix heatmap)

Plots include:
- ROC curve comparison
- PCA cumulative explained variance
- 2D PCA projection
- Confusion matrix heatmap

## Tools & Libraries
- Python
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
