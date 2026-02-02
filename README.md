# Advanced_time_series_forecasting__with_prophet_and_bayesian_optimization

## Project Overview

This project implements an advanced time series forecasting pipeline using Facebook Prophet combined with Bayesian Optimization (Optuna) to improve forecasting accuracy beyond default model configurations.

A complex synthetic time series dataset is generated to simulate real-world scenarios such as sales forecasting, stock price prediction, or electricity demand estimation. The dataset includes multiple seasonal patterns, a long-term trend, random noise, and injected anomalies. The performance of a baseline Prophet model is compared against an optimized model using standard evaluation metrics.

---

## Objectives

- Generate a complex multi-seasonal time series dataset
- Build a baseline Prophet forecasting model
- Apply Bayesian Optimization to tune Prophet hyperparameters
- Train a final optimized Prophet model
- Compare baseline and optimized models using evaluation metrics
- Visualize forecasting results

---

## Technologies Used

- Python  
- Facebook Prophet  
- Optuna (Bayesian Optimization)  
- NumPy  
- Pandas  
- Scikit-learn  
- Matplotlib  

---

## Project Workflow

### 1. Synthetic Data Generation
A daily time series dataset is generated with:
- Linear trend  
- Yearly seasonality  
- Weekly seasonality  
- Gaussian noise  
- Artificial anomalies (spikes and dips)  

---

### 2. Data Splitting
The dataset is divided into:
- Training set (70%)
- Validation set (15%)
- Test set (15%)

---

### 3. Baseline Model
A baseline Prophet model is trained using default parameters. Performance metrics are calculated on the validation dataset.

---

### 4. Bayesian Optimization
Bayesian Optimization is performed using Optuna to minimize RMSE by tuning the following hyperparameters:
- seasonality_prior_scale  
- changepoint_prior_scale  
- holidays_prior_scale  

This approach efficiently searches the hyperparameter space compared to traditional tuning methods.

---

### 5. Final Optimized Model
The optimized model is trained using the best hyperparameters identified through Bayesian Optimization and evaluated on the test dataset.

---

### 6. Evaluation Metrics

The following metrics are used for model evaluation:
- RMSE (Root Mean Squared Error)  
- MAE (Mean Absolute Error)  
- WAPE (Weighted Absolute Percentage Error)  

---

### 7. Results Comparison
A comparative analysis highlights the performance improvements achieved by the optimized model over the baseline Prophet model.

---

### 8. Visualization
The final output includes a plot comparing actual values with optimized forecast values.

---

## How to Run

### Install Dependencies
```bash
pip install prophet optuna scikit-learn pandas numpy matplotlib
