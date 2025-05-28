# stock_forecast_rolling_arima_LSTM_BiLSTM
# 📊 Time Series Forecasting with ARIMA and LSTM

Forecasting future values from historical time series data is essential in domains like finance, economics, and strategic planning. Traditional models such as **ARIMA** (AutoRegressive Integrated Moving Average) have been widely used for their strength in modeling linear and stationary time series. However, they struggle with capturing non-linear patterns, volatility, and long-term dependencies.

Modern deep learning techniques — particularly **Long Short-Term Memory (LSTM)** networks — address these challenges by retaining information over longer sequences through specialized memory gates. This makes LSTM well-suited for dynamic and complex forecasting tasks that require modeling temporal dependencies and non-linearities.

---

## 🧪 Project Overview

This project compares the performance of ARIMA and LSTM models across **nine diverse time series datasets**, including:

### 5 Stock Market Indices
- **Nikkei 225 (N225)**
- **NASDAQ Composite (IXIC)**
- **Hang Seng Index (HSI)**
- **S&P 500 (GSPC)**
- **Dow Jones Industrial Average (DJI)**

### 4 U.S. Macroeconomic Indicators
- **Medical Care Index (MC)**
- **Housing Index (HO)**
- **Trade-Weighted U.S. Dollar Index (EX)**
- **Money Stock (M1) Index (MS)**

> For stock market datasets, **only the 'Close' price column** was used as the predictive feature.

Each time series was split into training and testing sets (**70%/30%**), and a **rolling forecasting algorithm** was implemented to make one-step-ahead predictions, retraining the model after each new observation. This approach yields more accurate and responsive forecasts than static ARIMA or standard LSTM models.

---

## 🔍 Key Results

- **Overall accuracy improvement**: 70–75% using LSTM over ARIMA.
- **Stock indices**: Highly volatile, showed ~86% improvement.
- **Macroeconomic indices**: More stable, showed ~50% improvement — suggesting ARIMA may still be effective in such cases.
- **Additional layers** (BiLSTM, CNN, Dropout): Provided only marginal gains, confirming that the rolling LSTM alone captures most of the benefit.

---

## 🚀 Future Extensions

### Interactive Prediction Interface
Enable users to dynamically select:
- The number of lagged observations (look-back window)
- The forecast horizon (how many steps ahead to predict)

### Multi-Feature Learning with CNN
Extend the model to incorporate multiple features from stock data, such as:
- **Open, High, Low, Close, Volume**

Use **Convolutional Neural Networks (CNNs)** to extract spatial and temporal dependencies across all columns for more accurate predictions.

---

## 📌 Conclusion

> **Rolling LSTM forecasting significantly outperforms ARIMA for volatile time series data. Simpler is often better — further architectural complexity yields limited additional benefit. For stable, linear trends, traditional models still remain a strong choice.**
