# Code folder
This folder contains the analysis script for predictive modeling of fatal outcomes in commercial aviation accidents using NTSB data (2008-2024).
## File
`Final_Report_[Pham].qmd` - Complete analysis pipeline including data preprocessing, MICE imputation, exploratory analysis, LASSO logistic regression with year fixed effects, Random Forest modeling, and performance evaluation

## Required Libraries
Data manipulation and visualization
library(tidyverse)
library(dplyr)
library(tibble)

Regression modeling
library(fixest)        # Fixed effects models
library(glmnet)        # LASSO regularization
library(gglasso)       # Group LASSO
library(glinternet)    # Interaction models

Machine learning
library(randomForest)  # Random Forest classification
library(caret)         # Model training and evaluation

Missing data
library(mice)          # Multiple imputation

Model diagnostics
library(car)           # VIF analysis
library(pROC)          # ROC curves and AUC
library(ggfortify)     # Model diagnostics plots
library(leaps)         # Variable selection

Tables and output
library(modelsummary)  # Regression tables
library(knitr)         # Report generation
library(kableExtra)    # Enhanced tables
library(flextable)     # Flexible tables
library(officer)       # Document formatting

## Usage
- Install required packages: install.packages(c("tidyverse", "fixest", "glmnet", ...))
- Set working directory to project root
- Run `Final_Report_[Pham].qmd` to reproduce the complete analysis
- Outputs automatically saved to results/ folder

## Key Outputs
- Models: LASSO logistic regression (year FE) and Random Forest
- Figures: Correlation heatmap, VIF chart, ROC curves
- Tables: Regression coefficients, feature importance, performance metrics
- Performance: Accuracy, precision, recall, F1-score, AUC

## Reproducibility
Script uses set.seed(123) for reproducible results. LASSO lambda optimized via cross-validation. Random Forest trained with 500 trees.
