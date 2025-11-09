# DA401 Capstone Project - Nguyen Pham 

## Project Title
Predictive Modeling of Fatal Outcomes in Commercial Aviation Accidents

## Research Question
Between Logistic Regression and Random Forest, which model offers superior predictive performance for fatal accidents in commercial aviation, and which risk factors are most influential according to the Logistic Regression model? 

## Data Source
This project utilizes data from the National Transportation Safety Board (NTSB) database, comprising 1,388 commercial aviation accident records spanning 2008 to 2024. The dataset includes information on human factors (crew characteristics), environmental conditions (weather, visibility), and operational contexts (flight phase, regulatory classification).

## Methods
The analysis employs complementary predictive modeling approaches:
- Data Preprocessing: Multiple Imputation by Chained Equations (MICE) for missing data handling, with preservation of natural class distribution (8% fatal accidents) to maintain accurate risk calibration
- Modeling Approaches: Logistic Regression with LASSO regularization and year fixed effects. Random Forest classification with feature importance analysis. 
- Evaluation Metrics: Model performance assessed using accuracy, precision, recall, F1-score, and AUC-ROC curves, with emphasis on minority class (fatal accident) prediction
Statistical Analysis: Pearson correlation and Variance Inflation Factors (VIF) to assess multicollinearity

## Expected Timeline
- Phase 1 (September 9-18): Data cleaning, SQL data aggregation, and literature review
- Phase 2 (September 23-October 7): Exploratory data analysis, correlation analysis, model development (Logistic Regression and Random Forest), and performance comparison
- Phase 3 (October 9-December 11): Model refinement, interpretation of results, visualization generation, and manuscript drafting with peer review
- Phase 4 (December 15): Final presentation and submission of research paper with reproducible analysis scripts

## Repository Structure
- code/: R scripts for data preprocessing, model estimation, and performance evaluation
- writing/: Research proposal, literature review, manuscript drafts, and final paper
- results/: Model outputs, performance metrics, ROC curves, and figures
- data/: NTSB accident database (raw) and data dictionary

## Policy Implications
Findings provide empirical justification for:
- Enhanced regulatory oversight and resource allocation to FAR Part 135 operations.
- Phase-specific safety interventions prioritizing initial climb and critical flight segments
- Continued emphasis on weather-related decision protocols for instrument meteorological conditions
