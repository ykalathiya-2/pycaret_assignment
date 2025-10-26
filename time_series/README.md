# Time Series Forecasting (Weather Prediction)

## Overview
This folder contains minimal PyCaret workflows for **time series forecasting** on Delhi climate data, demonstrating both univariate approaches.

## Dataset
- **File:** `DailyDelhiClimateTrain.csv`
- **Period:** January 1, 2013 to April 24, 2017
- **Location:** Delhi, India
- **Features:** 
  - `date` - Timestamp
  - `meantemp` - Mean temperature (target variable)
  - `humidity` - Humidity level
  - `wind_speed` - Wind speed
  - `meanpressure` - Mean atmospheric pressure
- **Purpose:** Weather forecasting for Indian climate

## Tasks
This notebook demonstrates two forecasting approaches:

### 1. Univariate Forecasting WITHOUT Exogenous Variables
- Forecasts `meantemp` based solely on its historical values
- Uses only the time series pattern (trend, seasonality)

### 2. Univariate Forecasting WITH Exogenous Variables
- Forecasts `meantemp` using its history AND external predictors
- Incorporates `humidity`, `wind_speed`, and `meanpressure` as exogenous features
- Captures relationships between weather variables

## Notebook
- **File:** `time_series.ipynb`
- **Workflow:**
  1. Load and prepare the climate dataset
  2. **Experiment 1 (No Exog):**
     - Setup with meantemp as a univariate series
     - Compare time series models
     - Forecast next 14 days
     - Save model
  3. **Experiment 2 (With Exog):**
     - Setup with meantemp + exogenous features
     - Compare models with external regressors
     - Forecast next 14 days
     - Save model

## How to Run
1. Ensure PyCaret with time series extras is installed:
   ```bash
   pip install "pycaret[time_series]"
   ```

2. Open and run `time_series.ipynb` in Jupyter:
   ```bash
   jupyter notebook time_series.ipynb
   ```

3. Run all cells in order. The notebook will:
   - Load `DailyDelhiClimateTrain.csv`
   - Train two separate forecasting experiments
   - Generate 14-day forecasts for each
   - Save both trained models

## Model Output
- **Without exog:** `best_ts_univariate_no_exog.pkl` (excluded from Git)
- **With exog:** `best_ts_univariate_with_exog.pkl` (excluded from Git)
- Forecast DataFrames with predicted temperature values

## Evaluation Metrics
- MASE (Mean Absolute Scaled Error)
- RMSE (Root Mean Squared Error)
- MAE (Mean Absolute Error)
- Coverage (prediction interval coverage)
- SMAPE (Symmetric Mean Absolute Percentage Error)

## Models Compared
PyCaret automatically compares multiple forecasting algorithms:
- ARIMA / AutoARIMA
- Exponential Smoothing (ETS)
- Theta
- Naive / Seasonal Naive
- Prophet (if installed)
- TBATS
- And more...

## Use Case
Weather forecasting enables:
- Agricultural planning and crop management
- Energy demand prediction
- Transportation and logistics optimization
- Public health preparedness
- Tourism and event planning

## References
- [PyCaret Time Series Tutorial](https://colab.research.google.com/github/pycaret/pycaret/blob/master/tutorials/Tutorial%20-%20Time%20Series%20Forecasting.ipynb)

## Dataset Attribution
- Source: Weather Underground API
- Academic use: Assignment 4, Data Analytics Course 2019, PES University, Bangalore
