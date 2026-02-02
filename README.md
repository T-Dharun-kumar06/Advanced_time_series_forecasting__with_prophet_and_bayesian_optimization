Advanced_time_series_forecasting__with_prophet_and_bayesian_optimization
📌 Project Overview

This project demonstrates an advanced time series forecasting pipeline using Facebook Prophet combined with Bayesian Optimization (Optuna) to achieve improved forecasting accuracy beyond default model settings.

The main objective is to move past baseline forecasting by systematically tuning Prophet’s hyperparameters and evaluating performance using robust time series metrics such as RMSE, MAE, and WAPE.

The project uses a synthetically generated complex dataset that includes:

Multiple seasonal patterns

Long-term trend

Random noise

Injected anomalies (spikes and dips)

This setup closely simulates real-world business time series data such as electricity demand, stock prices, or sales forecasting.

🎯 Key Objectives

Generate a complex multi-seasonal time series dataset

Build a baseline Prophet model using default parameters

Apply Bayesian Optimization to tune Prophet hyperparameters

Train a final optimized Prophet model

Compare baseline vs optimized models using standard evaluation metrics

Visualize forecast results

🧠 Technologies Used

Python

Facebook Prophet

Optuna (Bayesian Optimization)

NumPy & Pandas

Scikit-learn

Matplotlib

📂 Project Workflow
1️⃣ Synthetic Data Generation

A daily time series dataset is programmatically created with:

Linear trend

Yearly seasonality

Weekly seasonality

Gaussian noise

Five artificial anomalies (spikes/dips)

This ensures the model is tested on a challenging and realistic dataset.

2️⃣ Data Splitting

The dataset is divided into:

Training set (70%)

Validation set (15%)

Test set (15%)

This allows fair model evaluation and prevents data leakage.

3️⃣ Baseline Model

A baseline Prophet model is trained using default configuration:

Yearly seasonality enabled

Weekly seasonality enabled

Daily seasonality disabled

Baseline performance metrics are computed on the validation set.

4️⃣ Bayesian Optimization with Optuna

Bayesian Optimization is applied to efficiently search the hyperparameter space and minimize RMSE.

Optimized parameters include:

seasonality_prior_scale

changepoint_prior_scale

holidays_prior_scale

Optuna intelligently balances exploration and exploitation, making it more efficient than grid or random search.

5️⃣ Final Optimized Model

Using the best hyperparameters found by Optuna:

The model is retrained on training + validation data

Forecasts are generated for the test set

Final performance metrics are computed

6️⃣ Evaluation Metrics

The following metrics are used for comparison:

RMSE (Root Mean Squared Error)

MAE (Mean Absolute Error)

WAPE (Weighted Absolute Percentage Error)

These metrics provide a comprehensive view of forecasting accuracy and robustness.

7️⃣ Results Comparison

A side-by-side comparison clearly shows the performance gains achieved through Bayesian Optimization over the baseline Prophet model.

8️⃣ Visualization

The final section visualizes:

Actual test values

Optimized Prophet forecasts

This helps in visually validating model performance.

📊 Sample Output

Baseline vs Optimized performance table

Best hyperparameters identified by Optuna

Forecast plot comparing predicted and actual values

🚀 How to Run the Project
Install Dependencies
pip install prophet optuna scikit-learn pandas numpy matplotlib

Run the Script
python main.py

✅ Key Takeaways

Default forecasting models can often be significantly improved with proper tuning

Bayesian Optimization provides an efficient and scalable approach for hyperparameter search

Prophet is highly effective for multi-seasonal time series with anomalies

A structured evaluation strategy ensures reliable and reproducible results

📌 Future Enhancements

Add real-world datasets (electricity load, sales, stock prices)

Introduce holiday effects

Compare Prophet with ARIMA, SARIMA, or LSTM models

Use cross-validation instead of single validation split

👤 Author

Dharun Kumar T
Advanced Time Series Forecasting Project
