# 📈 Multivariate Stock Price Predictor

A Deep Learning project that predicts stock prices (AAPL) using Long Short-Term Memory (LSTM) networks. Unlike basic models, this uses **Multivariate Time Series** analysis, combining raw price data with Technical Indicators (Moving Averages).

## 🧠 The Architecture
* **Model:** Stacked LSTM (2 Layers) + Dropout (to prevent overfitting).
* **Input Features:** 1.  **Close Price:** The daily closing value.
    2.  **MA50 (50-Day Moving Average):** A technical indicator used to identify trend direction.
* **Sequence Length:** 60 Days (The model looks at the past 2 months to predict tomorrow).

## 🛠 Tech Stack
* **Python**
* **TensorFlow / Keras** (Deep Learning)
* **yfinance** (Live Market Data API)
* **Scikit-Learn** (MinMax Scaling)

## 📊 Key Concepts
* **Time Series Windowing:** Created a "sliding window" of data to preserve temporal order.
* **Multivariate Input:** The LSTM processes multiple parallel data streams (Price + Trends) simultaneously to improve context.
* **Stationarity & Scaling:** Implemented MinMax scaling to normalize data between 0 and 1 for faster convergence.

## 🚀 Usage
1.  Run the notebook to fetch the latest 5 years of AAPL data.
2.  The script automatically calculates the MA50 technical indicator.
3.  View the prediction graph comparing Actual vs. Predicted prices.
