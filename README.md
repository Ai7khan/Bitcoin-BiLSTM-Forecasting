# Bitcoin-BiLSTM-Forecasting
Deep Learning pipeline for Crypto volatility forecasting and Portfolio Optimization.
# Deep Learning for Cryptocurrency Forecasting & Portfolio Optimization 📉🚀

## 📌 Project Overview
This project implements a comprehensive FinTech pipeline that predicts Bitcoin volatility using **Deep Learning (Bi-LSTM)** and constructs a hedged portfolio using **Modern Portfolio Theory (Markowitz Optimization)**.

Unlike traditional linear models (ARIMA), this approach captures "Fat Tail" risks in cryptocurrency markets by integrating **On-Chain Blockchain Metrics** (Hash Rate) and **GARCH Volatility** estimates directly into the Neural Network.

## 🏗️ Architecture
The pipeline consists of three main stages:
1.  **Data Engineering:** Merging Market Data (Yahoo Finance) with On-Chain Data (Blockchain.com) and engineering features like RSI, MACD, and GARCH volatility.
2.  **Predictive Modeling:** A **Bidirectional LSTM (Bi-LSTM)** network trained on Log Returns to forecast market direction.
    * *Baseline Error (MAE):* $5,427
    * *Optimized Error (MAE):* **$1,596** (~1.6% relative error)
3.  **Portfolio Optimization:** A Monte Carlo simulation (5,000 iterations) determines the optimal asset allocation (Efficient Frontier) between Bitcoin, Gold, and the S&P 500.

## 📊 Key Results
* **Accuracy:** Achieved a **70% reduction** in forecasting error compared to baseline models.
* **Strategy:** The AI identified a "Bearish Correction" (-3.5%) horizon, leading to a defensive portfolio allocation:
    * **Bitcoin:** 40% (Growth Engine)
    * **Gold:** 31% (Volatility Hedge)
    * **S&P 500:** 29% (Stability)

## 🛠️ Tech Stack
* **Python 3.10+**
* **TensorFlow/Keras:** For building the Bi-LSTM Neural Network.
* **SciPy:** For Mean-Variance Portfolio Optimization.
* **Pandas/NumPy:** Data manipulation and interpolation.
* **Matplotlib/Seaborn:** Visualization of Efficient Frontier and Forecasts.
* **Arch:** For GARCH volatility modeling.

## 🚀 How to Run
1.  Clone the repository:
    ```bash
    git clone [https://github.com/YOUR_USERNAME/Bitcoin-BiLSTM-Forecasting.git](https://github.com/YOUR_USERNAME/Bitcoin-BiLSTM-Forecasting.git)
    ```
2.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3.  Run the Jupyter Notebook:
    ```bash
    jupyter notebook "Bitcoin_Forecasting_Project.ipynb"
    ```

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
