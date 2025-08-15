# Macroeconomic Regime Classification with Machine Learning

## Project Overview
This project focuses on classifying macroeconomic regimes (growth, recession, crisis) using machine learning applied to multi-factor time series data. By engineering relevant features and training robust models, the project identifies economic regimes to support investment decision-making and risk management. Advanced feature engineering and model optimization are used to achieve high predictive performance.

## Objectives
- Engineer features from time series data to capture macroeconomic dynamics.  
- Train and compare multiple machine learning models for accurate regime classification.  
- Identify key drivers of classification to provide actionable insights.  

## Dataset
The dataset contains multi-factor time series data from macroeconomic sources such as FRED-MD and similar databases.  
- **Features**: GDP growth, yield curve spreads, inflation rates, volatility metrics, unemployment rates, and consumer sentiment.  
- **Target Variable**: Macroeconomic regime labels (growth, recession, crisis).  
- **Characteristics**: Time series with trends, seasonality, and non-stationarity.  

## Methodology

### Feature Engineering
- **Lag Features**: Lagged variables for key indicators to capture temporal dependencies.  
- **Yield Curve Spreads**: Calculated spreads (e.g., 10-year minus 2-year Treasury yields) as recession signals.  
- **Rolling Volatility**: Standard deviations over rolling windows to measure market instability.  
- **Additional Features**: Unemployment rates, consumer sentiment, and other macroeconomic indicators.  

### Data Preprocessing
- **Stationarity Handling**: Differencing and log transformations based on time series analysis.  
- **Normalization**: Standardized features for consistent scaling.  
- **Data Splitting**: Time-series-aware splitting to avoid data leakage.  

### Model Training and Evaluation
Models trained and tuned using 5-fold cross-validation with **GridSearchCV**:  
- **Logistic Regression**: Baseline classification model.  
- **Random Forest**: Captures non-linear relationships and interactions.  
- **XGBoost**: Gradient boosting for high performance on complex data.  
- **SVM**: Non-linear kernel classification.  

**Performance**:  
- **ROC-AUC**: 0.91  
- **Accuracy**: 88%  
- **Key Drivers**: Yield curve spread, GDP growth, and volatility.  

## Repository Structure
- **Macroeconomic_Regime_Classification.ipynb**: Full workflow including preprocessing, feature engineering, model training, evaluation, and analysis.  
- **Dataset File(s)**: Macroeconomic time series data (.csv, .xlsx).  
- **README.md**: Project overview.  

## Results
- Lag features, yield curve spreads, and rolling volatility improved predictive performance.  
- XGBoost or Random Forest achieved the highest ROC-AUC and accuracy after hyperparameter tuning.  
- Yield curve spread, GDP growth, and volatility were the most influential features, consistent with economic theory.  
- The model provides reliable classification to support investment strategies and risk management.  

## Requirements
```bash
pip install pandas numpy scikit-learn xgboost statsmodels scipy matplotlib seaborn
