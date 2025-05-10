# bike_rental_ml_forecast

![Bike Sharing](https://images.unsplash.com/photo-1556316384-12c35d30afa4?auto=format&fit=crop&q=80&w=800&h=300)

## Overview
This project uses statistical learning methods to predict bike rental demand using historical data from the Capital Bikeshare system in Washington, D.C. The analysis compares multiple modeling approaches, from linear regression to ensemble methods, to determine the most effective technique for this prediction task.

## Project Structure
```
BIKE_RENTAL_ML_FORECAST/
├── data/
│   └── raw/
│       └── day.csv
├── notebooks/
│   └── main-report.ipynb
└── README.md
```

## Dataset
The dataset comes from the UCI Machine Learning Repository and contains daily count data of rental bikes along with weather and seasonal information from 2011 to 2012. Key features include:

- Temporal information (date, season, year, month, weekday, holiday status)
- Weather conditions (temperature, humidity, windspeed, weather situation)
- Target variables (casual users, registered users, total count of rentals)

## Models Implemented
This project implements and compares the following models:

1. **Linear Regression**
   - Base implementation
   - Improved version addressing common regression problems
   
2. **Tree-based Methods**
   - Decision Trees
   - Bagging
   - Random Forest
   - XGBoost

3. **Ensemble**
   - Weighted combination of top-performing models

## Key Findings
- Ensemble methods outperform individual models, with the weighted ensemble achieving the best results
- Temperature-season interaction is the most important predictor of bike rental demand
- Weather variables strongly influence rental patterns, with clear non-linear relationships
- A well-implemented linear regression model can achieve surprisingly competitive results compared to more complex tree-based methods

## How to Run
1. Clone this repository
2. Install the required packages:
   ```
   pip install numpy pandas matplotlib seaborn scikit-learn xgboost optuna statsmodels
   ```
3. Open and run the Jupyter notebook:
   ```
   jupyter notebook notebooks/main-report.ipynb
   ```

## Technical Highlights
- Systematic approach to addressing the six common regression problems
- Feature engineering to capture temporal patterns and non-linear relationships
- Hyperparameter optimization using Optuna
- Model evaluation via cross-validation with RMSE and R² metrics
- Model ensemble techniques for improved prediction accuracy

## Results
The ensemble model achieved the best performance with a test RMSE of 1235.91 and R² of 0.619, outperforming individual models like XGBoost (RMSE: 1257.85, R²: 0.605) and Random Forest (RMSE: 1268.58, R²: 0.599).

## Author
Eddie Aguilar Ceballos

## License
This project is licensed under the MIT License - see the LICENSE file for details.
