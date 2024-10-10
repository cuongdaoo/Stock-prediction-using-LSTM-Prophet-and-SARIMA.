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
Here’s a brief summary of LSTM, Prophet, and SARIMA models, commonly used in stock price forecasting:

## 1. **LSTM (Long Short-Term Memory)**
   - **Overview:** LSTM is a type of recurrent neural network (RNN) designed to handle sequential data by learning long-term dependencies. It is especially useful in time series forecasting, as it addresses the vanishing gradient problem faced by traditional RNNs, allowing it to remember important patterns over time.
   - **How it works:** LSTM consists of memory cells that maintain information over long sequences of time steps. It uses gates (input, forget, and output gates) to regulate the flow of information, deciding what to keep, forget, or output at each step.
   - **Application in stock price prediction:** LSTM can capture long-term trends and short-term patterns from past stock prices, making it effective for complex time series with trends, seasonality, and irregular patterns.

## 2. **Prophet**
   - **Overview:** Prophet is a forecasting tool developed by Facebook, designed for business time series data. It is particularly useful for time series with daily observations and strong seasonal effects. Prophet is flexible and can handle missing data and large outliers.
   - **How it works:** Prophet models time series data as a sum of three components: trend, seasonality, and holidays (or other events). It uses piecewise linear or logistic growth models for trend, Fourier series to capture seasonality, and a list of known events (such as holidays) to account for special events.
   - **Application in stock price prediction:** While Prophet is more frequently used for business and marketing data, it can also model stock price trends and seasonality, particularly when stock prices exhibit consistent cycles or growth patterns.

## 3. **SARIMA (Seasonal AutoRegressive Integrated Moving Average)**
   - **Overview:** SARIMA is an extension of the ARIMA model, which is widely used for time series forecasting. SARIMA includes components to handle both seasonal and non-seasonal data, making it ideal for time series with repeating seasonal patterns.
   - **How it works:** SARIMA consists of several components:
     - **AR (AutoRegressive):** Relies on past values of the time series.
     - **I (Integrated):** Uses differencing to make the time series stationary.
     - **MA (Moving Average):** Models the relationship between the forecast and past forecast errors.
     - **Seasonal Component:** Adds seasonal terms to handle seasonality, allowing it to model both trends and cycles.
   - **Application in stock price prediction:** SARIMA can be used when stock price data shows clear seasonal patterns, such as annual or quarterly cycles. It helps model the dependencies between past and future stock prices, accounting for both short-term fluctuations and long-term trends.

# **Dataset**




