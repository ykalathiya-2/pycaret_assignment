# Regression (Car Price Prediction)

## Overview
This folder contains a minimal PyCaret workflow for **regression** to predict car prices based on vehicle characteristics.

## Dataset
- **File:** `CarPrice_Assignment.csv`
- **Features:** Various car attributes (make, model, engine specs, dimensions, etc.)
- **Target:** `price` - Car selling price
- **Purpose:** Model car prices to understand pricing dynamics in the automotive market

## Problem Statement
A Chinese automobile company (Geely Auto) wants to enter the US market and needs to understand:
- Which variables are significant in predicting car prices
- How well those variables describe price variations
- Insights for design and business strategy decisions

## Task
Supervised regression using PyCaret's AutoML to build a car price prediction model.

## Notebook
- **File:** `regression.ipynb`
- **Workflow:**
  1. Load and explore the car price dataset
  2. Set up PyCaret `RegressionExperiment` with normalization and transformation
  3. Compare multiple regression models automatically
  4. Evaluate the best model interactively
  5. Generate price predictions
  6. Save the trained model

## How to Run
1. Ensure PyCaret is installed:
   ```bash
   pip install pycaret[analysis]
   ```

2. Open and run `regression.ipynb` in Jupyter:
   ```bash
   jupyter notebook regression.ipynb
   ```

3. Run all cells in order. The notebook will:
   - Load `CarPrice_Assignment.csv`
   - Automatically compare 20+ regression algorithms
   - Select the best model based on R² and RMSE
   - Display interactive evaluation plots
   - Generate price predictions

## Model Output
- **Model file:** `best_car_price_model.pkl` (excluded from Git)
- Predictions with actual vs. predicted price comparisons

## Evaluation Metrics
- R² (coefficient of determination)
- RMSE (Root Mean Squared Error)
- MAE (Mean Absolute Error)
- MAPE (Mean Absolute Percentage Error)
- Residual plots

## Use Case
Car price prediction enables:
- Competitive pricing strategy
- Market positioning insights
- Feature importance analysis for design decisions
- Understanding price elasticity factors

## References
- [PyCaret Regression Tutorial](https://pycaret.gitbook.io/docs/get-started/tutorials)

## Note
This dataset is for educational purposes only and should not be used for real-world business decisions without further validation.
