# CARBON EMISSION PREDICTION

## Overview
This project presents a comprehensive machine learning framework to predict **CO₂ emissions per capita** for countries worldwide, based on key economic, demographic, and environmental indicators. Leveraging a Random Forest regression model, the system not only captures historical patterns but also forecasts future emissions using compound annual growth trends — offering actionable insights for policy and sustainability planning.

## Objective
To develop a data-driven model that accurately estimates CO₂ emissions per capita using selected macro-level indicators, and to project emission trends over the next two decades for informed climate strategy development.

## Dataset Summary
- **Dataset Source**: World Bank Climate Change Indicators  
- **Coverage**: Multiple countries (1990–2011) 

## Tools & Technologies
- **Language**: Python  
- **Libraries**: pandas, numpy, scikit-learn, seaborn, matplotlib, joblib  
- **Model**: RandomForestRegressor with recursive feature elimination and hyperparameter tuning  
- **Utilities**: RFECV, RandomizedSearchCV, cross-validation (KFold)

## Methodology

### Data Cleaning & Preprocessing
- Removed outliers to improve model generalization
- Selected the most impactful features based on domain relevance and RFECV
- Ensured reproducibility through consistent random seeds

### Feature Selection
- Applied recursive feature elimination with cross-validation (RFECV)
- Reduced dimensionality to core predictors that significantly influence CO₂ emissions

### Model Development
- Split data into training and test sets (80:20)
- Used RandomizedSearchCV to optimize hyperparameters for the Random Forest model
- Trained and evaluated model with 10-fold cross-validation for robustness

### Forecasting
- Computed CAGR for all selected features
- Projected future feature values for the next 20 years
- Predicted future CO₂ emissions for selected countries using the trained model

## Results

- **R² score (training cross-validation)**: 0.986  
- **R² score (test set)**: 0.986  
- **Model variance across folds**: < 0.004  
- Demonstrated stable performance across diverse regions and temporal splits  
- Forecast plots reveal:
  - Declining trends in developed nations 
  - Gradual growth in developing nations 
