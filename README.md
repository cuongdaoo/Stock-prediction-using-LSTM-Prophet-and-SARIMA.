**Topic: Stock-prediction-using-LSTM-Prophet-and-SARIMA.**\
# **Overview**
Forecasting is the prediction of future events based on certain data or foundations, playing an important role in science and management. Forecasting methods include qualitative (relying on expert opinions, useful when historical data is unavailable) and quantitative (based on mathematics and statistics, requiring historical data). Among them, time series forecasting is a specific method based on the assumption that past patterns will continue into the future, helping to model the relationship between independent and dependent variables to predict future values of the dependent variable.
# **Characteristics of Time Series Data**
**A time series** is a sequence of data points measured at successive time intervals with a consistent frequency. In general forecasting problems, especially in stock price forecasting, the data used is time series data. Time series data consists of observations from a random process recorded in chronological order. Examples include daily stock prices, daily sales revenue, monthly electricity consumption, etc. The advantage of time series data is its ability to store a field's state over time, allowing important insights for future forecasting. Thus, time series data plays a crucial role in development.

A time series consists of several components:
- **Stationary Data:** A time series is considered stationary if its mean and variance do not change over time, and the covariance between two time periods depends only on the distance or time lag, not on the actual time.
  - It shows a tendency to return to a mean value, fluctuating around a fixed long-term average.
  - The variance is constant over time.
  - The autocorrelation function decreases as the lag increases.
  
- **Trending Data:** This reflects changes in data over time, such as the growing global population or the Earth's rising temperature.
  
- **Seasonal Data:** This represents cyclic behavior based on the calendar year. Seasonal time series are non-stationary, and the simplest method to remove seasonality is by taking the mth difference.
  
- **Cyclic Data:** This reflects repeating patterns in data over time, influenced by cycles such as weather, animal growth, and human consumer behavior. Identifying cycles helps in more accurate forecasting.
# **Model**

* Prophet: A time series forecasting model developed by Facebook, designed to be user-friendly and effective for data with seasonal trends and cycles. Prophet is flexible, handles missing data well, and is good at modeling long-term trends and outliers.

* SARIMA (Seasonal ARIMA): An extension of the ARIMA (AutoRegressive Integrated Moving Average) model, incorporating a seasonal component to handle cyclic data. SARIMA combines autoregressive, moving average, and differencing terms, along with seasonal factors for forecasting.

* LSTM (Long Short-Term Memory): A type of deep recurrent neural network (RNN) used for time series data. LSTM excels at retaining both long-term and short-term dependencies, making it effective for forecasting complex and nonlinear sequences.

# **Dataset**
The dataset is the price and volume data of the stock code HPG starting from 01-01-2019 to 01-04-2024\
The reason for choosing such a time period is because:
During this period, there were 3 phases: **down-trend, sideway, uptrend**.\
- 2019-2020: Down-trend phase
- 2020-2021: Sideway phase
- 2021-2022: Up-trend phase
Thus, the data will cover the main stages of the stock market, helping the model predict more accurately under different conditions.\
![Train data (80%) (1)](https://github.com/user-attachments/assets/1242e95e-01b0-4566-96bb-6bb081b05f1e)

# **Result**
Model prediction charts:
- Prophet\
![image](https://github.com/user-attachments/assets/16b6a46f-ac81-463e-a081-40779ec08e13)
- LSTM\
![image](https://github.com/user-attachments/assets/493fcb2c-e4ac-441b-ae01-298c72b6e45e)
- SARIMA\
![newplot](https://github.com/user-attachments/assets/0a01a515-67cd-44e1-a584-29c9ba952c12)

Forecast results:
| Model   | R^2        | MAE         | MAPE     | MSE           | RMSE       |
|---------|------------|-------------|----------|---------------|------------|
| LSTM    | 0.401463   | 390.218034  | 0.014253 | 2.623775e+05  | 512.227957 |
| Prophet | -4.716500  | 2666.463405 | 0.101897 | 7.490235e+06  | 2736.829365|
| SARIMA  | -197.576265| 16110.646623| 0.610972 | 2.601912e+08  | 16130.442339|











