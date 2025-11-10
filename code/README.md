# Code folder
This folder contains the analysis script for predictive modeling of fatal outcomes in commercial aviation accidents using NTSB data (2008-2024).
## File
- `data.sqbpro` - SQL file for data cleaning, merging, selecting variables, and filtering commercial aircraft accidents
- `Final_Report_[Pham].qmd` - Complete analysis pipeline including data preprocessing, MICE imputation, exploratory analysis, LASSO logistic regression with year fixed effects, Random Forest modeling, and performance evaluation

## Required Libraries
### Data Manipulation and Visualization
- `tidyverse`, `dplyr`, `tibble`

### Regression Modeling
- `fixest` (Fixed effects models)
- `glmnet` (LASSO regularization)
- `gglasso` (Group LASSO)
- `glinternet` (Interaction models)

### Machine Learning
- `randomForest` (Random Forest classification)
- `caret` (Model training and evaluation)

### Missing Data Handling
- `mice` (Multiple imputation)

### Model Diagnostics
- `car` (VIF analysis)
- `pROC` (ROC curves and AUC)
- `ggfortify` (Diagnostic plots)
- `leaps` (Variable selection)

### Tables and Reporting
- `modelsummary` (Regression tables)
- `knitr` (Report generation)
- `kableExtra` (Enhanced tables)
- `flextable` (Flexible tables)
- `officer` (Document formatting)

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
