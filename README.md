# House Price Prediction

A comprehensive Machine Learning project to predict house prices using Python and scikit-learn.

## Project Overview

This project implements a complete machine learning pipeline for predicting house prices. The analysis includes exploratory data analysis (EDA), feature engineering, and model comparison between multiple regression algorithms.

### Dataset Information
- **Rows:** 545 house records
- **Target Variable:** price (House Price)
- **Features:** 12 features including area, bedrooms, bathrooms, and amenities

### Features

**Numerical Features:**
- area - House area in square feet
- bedrooms - Number of bedrooms
- bathrooms - Number of bathrooms
- stories - Number of stories
- parking - Number of parking spaces

**Categorical Features:**
- furnishingstatus - Furnishing status (furnished, semi-furnished, unfurnished)

**Binary Features:**
- mainroad - Near main road (yes/no)
- guestroom - Has guest room (yes/no)
- basement - Has basement (yes/no)
- hotwaterheating - Has hot water heating (yes/no)
- airconditioning - Has air conditioning (yes/no)
- prefarea - In preferred area (yes/no)

## Pipeline Overview

1. **Import Required Libraries** - Load all necessary packages
2. **Load Dataset** - Read and explore the CSV file
3. **Missing Data Handling** - Check and impute missing values
4. **Duplicate Data Handling** - Identify and remove duplicates
5. **Categorical Encoding** - Convert categorical variables to numerical
6. **Exploratory Data Analysis (EDA)** - Statistical analysis and visualizations
7. **Outlier Handling** - Detect and treat outliers using IQR method
8. **Feature Engineering** - Create new features from existing data
9. **Feature Reduction** - Apply correlation analysis and PCA
10. **Model Building & Evaluation** - Train and compare multiple models

## Models Used

- **Linear Regression** - Simple linear relationship between features and price
- **Random Forest Regressor** - Ensemble method for robust predictions

## Key Metrics

The models are evaluated using:
- **Mean Squared Error (MSE)** - Average squared error between actual and predicted values
- **Root Mean Squared Error (RMSE)** - Square root of MSE for interpretability
- **Mean Absolute Error (MAE)** - Average absolute error
- **R² Score** - Coefficient of determination (0-1 scale, higher is better)

## Feature Engineering

The notebook creates several new features:
- **price_per_area** - Price per unit area (proxy for price density)
- **total_rooms** - Total number of bedrooms and bathrooms
- **luxury_features** - Count of luxury amenities (hot water heating, air conditioning)
- **has_premium_features** - Binary indicator for premium features (basement, guest room, preferred area)

## Dimensionality Reduction

- **Correlation Analysis** - Identify features with strong correlation to price
- **Principal Component Analysis (PCA)** - Reduce feature dimensionality while preserving variance

## Results & Insights

The notebook provides:
- Comprehensive model comparison with visualizations
- Feature importance rankings
- Actual vs. Predicted price scatter plots
- Recommendation on best-performing model

## Requirements

See `requirements_housing.txt` for all dependencies.

### Key Libraries

- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computing
- **matplotlib** - Data visualization
- **seaborn** - Statistical data visualization
- **scipy** - Scientific computing
- **scikit-learn** - Machine learning algorithms
- **jupyter** - Interactive notebook environment

## Installation

1. Clone or download the project
2. Install required packages:
```bash
pip install -r requirements_housing.txt
```

## Usage

1. Ensure the `Housing.csv` file is in the same directory as the notebook
2. Open the notebook in Jupyter:
```bash
jupyter notebook House_Price_Prediction.ipynb
```
3. Run cells sequentially from top to bottom
4. Examine visualizations and model metrics for insights

## Files

- **House_Price_Prediction.ipynb** - Main analysis notebook with all steps
- **Housing.csv** - Dataset with house price records
- **requirements_housing.txt** - Python package dependencies

## Performance Summary

The models' performance is evaluated on the test set:

| Metric | Linear Regression | Random Forest |
|--------|------------------|---------------|
| RMSE | Calculated | Calculated |
| MAE | Calculated | Calculated |
| R² Score | Calculated | Calculated |

*Note: Exact values are calculated when the notebook is run*

## Future Improvements

- Implement more advanced models (Gradient Boosting, XGBoost)
- Hyperparameter tuning for better performance
- Cross-validation for more robust evaluation
- Feature selection using mutual information
- Ensemble methods combining multiple models

## Author

Created for machine learning project demonstration

## License

Open for educational and personal use
