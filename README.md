**Topic: Stock-prediction-using-LSTM-Prophet-and-SARIMA.**\
# **Overview**
Forecasting is the prediction of future events based on certain data or foundations, playing an important role in science and management. Forecasting methods include qualitative (relying on expert opinions, useful when historical data is unavailable) and quantitative (based on mathematics and statistics, requiring historical data). Among them, time series forecasting is a specific method based on the assumption that past patterns will continue into the future, helping to model the relationship between independent and dependent variables to predict future values of the dependent variable.
# **Characteristics of Time Series Data**
**A time series** is a sequence of data points measured at successive time intervals with a consistent frequency. In general forecasting problems, especially in stock price forecasting, the data used is time series data. Time series data consists of observations from a random process recorded in chronological order. Examples include daily stock prices, daily sales revenue, monthly electricity consumption, etc. The advantage of time series data is its ability to store a field's state over time, allowing important insights for future forecasting. Thus, time series data plays a crucial role in development.
**Summary in English:**

**Characteristics of Time Series Data:**
A time series is a sequence of data points measured at successive time intervals with a consistent frequency. In general forecasting problems, especially in stock price forecasting, the data used is time series data. Time series data consists of observations from a random process recorded in chronological order. Examples include daily stock prices, daily sales revenue, monthly electricity consumption, etc. The advantage of time series data is its ability to store a field's state over time, allowing important insights for future forecasting. Thus, time series data plays a crucial role in development.

A time series consists of several components:
- **Stationary Data:** A time series is considered stationary if its mean and variance do not change over time, and the covariance between two time periods depends only on the distance or time lag, not on the actual time.
  - It shows a tendency to return to a mean value, fluctuating around a fixed long-term average.
  - The variance is constant over time.
  - The autocorrelation function decreases as the lag increases.
  
- **Trending Data:** This reflects changes in data over time, such as the growing global population or the Earth's rising temperature.
  
- **Seasonal Data:** This represents cyclic behavior based on the calendar year. Seasonal time series are non-stationary, and the simplest method to remove seasonality is by taking the mth difference.
  
- **Cyclic Data:** This reflects repeating patterns in data over time, influenced by cycles such as weather, animal growth, and human consumer behavior. Identifying cycles helps in more accurate forecasting.



