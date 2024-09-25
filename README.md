# Cisco (CSCO) Stock Price Forecast Using LSTM
This project involves developing an LSTM model to forecast Cisco's stock price, focusing on univariate time series data. The dataset spans from 1990 to 2020, with a primary focus on the Date and Close columns (Close refers to the closing price). The objective is to forecast the stock price for the upcoming Monday based on data from the previous week (Monday to Friday).

## Model Overview
A windowing technique was applied, using a 5-day input window (Monday to Friday stock prices) to forecast the price for the next Monday (horizon = 1).

## Models Developed
1. Baseline Model:
- A simple LSTM with 50 units and ReLU activation.
- A Dense layer for prediction.
2. Tuned Model:
- Hyperparameter tuning of LSTM units (32 to 128) and learning rates (1e-2, 1e-3, 1e-4) was performed.
- The best configuration: 32 LSTM units with a learning rate of 0.01.

## Model Performance
<img width="700" alt="image" src="https://github.com/user-attachments/assets/d0b82574-2c75-41f5-b0ac-9dd55a4581e1">

## Model Evaluation Metrics: RMSE, MAE, and MAPE
In this project, three key metrics—RMSE, MAE, and MAPE—were used to evaluate the performance of both the baseline and tuned LSTM models for forecasting Cisco's stock price.

- RMSE (Root Mean Squared Error): RMSE measures the square root of the average squared errors between predicted and actual values. The tuned model achieved an RMSE of 1.0269, lower than the baseline model's RMSE of 1.0951, indicating that the tuned model had smaller overall prediction errors and was more accurate in forecasting CSCO's close price.

- MAE (Mean Absolute Error): MAE represents the average of the absolute differences between predicted and actual values. The tuned model's MAE was 0.6755, compared to the baseline's MAE of 0.7524, reflecting that the tuned model had consistently smaller prediction errors and provided predictions closer to the actual close price.

- MAPE (Mean Absolute Percentage Error): MAPE measures the average percentage of absolute errors between predicted and actual values. The tuned model achieved a MAPE of 1.5567%, outperforming the baseline model's MAPE of 1.7349%. This shows that the tuned model had a smaller relative percentage error, further highlighting its superior performance.

The decrease in RMSE, MAE, and MAPE values demonstrates that hyperparameter tuning significantly improved the model’s accuracy and reliability in predicting CSCO’s close price. These metrics confirm that the tuned model outperforms the baseline in time series forecasting.

## Conclusion
The tuned LSTM model, with 32 units and a learning rate of 0.01, provides better forecasting performance than the baseline model for Cisco's stock price.
