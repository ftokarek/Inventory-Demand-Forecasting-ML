# Inventory Demand Forecasting

A machine learning project for predicting sales demand using time series data with feature engineering and multiple regression models.

## Dataset

The dataset contains 913,000 records with the following features:
- `date`: Date of sales (2013-2017)
- `store`: Store identifier (10 unique stores)
- `item`: Item identifier (50 unique items)
- `sales`: Daily sales quantity (target variable)

## Methodology

### Data Preprocessing
- **Feature Engineering**: Created temporal features including year, month, day, weekday, and weekend indicators
- **Holiday Detection**: Integrated Indian holidays using the `holidays` library
- **Cyclical Encoding**: Applied sine/cosine transformations for monthly seasonality
- **Outlier Removal**: Filtered sales values above 140 to remove extreme outliers

### Exploratory Data Analysis
- Sales distribution analysis with histograms and box plots
- Time series visualization with moving averages
- Correlation analysis between features
- Sales patterns by store, month, weekday, and holiday status

### Model Training
- **Data Split**: 95% training, 5% validation with random state for reproducibility
- **Feature Scaling**: StandardScaler normalization applied to all features
- **Model Comparison**: Tested four regression algorithms:
  - Linear Regression
  - XGBoost Regressor
  - Lasso Regression
  - Ridge Regression

## Results

XGBoost Regressor achieved the best performance:
- Training MAE: 6.92
- Validation MAE: 6.93


