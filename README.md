# LSTM-Based Stock Price Prediction Using Deep Learning

This repository contains a detailed implementation of a stock price prediction model leveraging Long Short-Term Memory (LSTM) networks. The project is designed to predict future stock prices based on historical data and provides visualizations to analyze the model's performance. 

---

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Results](#results)
- [Contributions](#contributions)
- [License](#license)

---

## Introduction

Stock price prediction is a challenging problem due to the volatility and non-linear trends in financial markets. This project implements an LSTM-based neural network, which is well-suited for time-series analysis. The model is trained on 20 years of historical stock data from Google, obtained using the Yahoo Finance API, to predict future closing prices.

---

## Features

1. **Data Collection**:
   - Utilizes Yahoo Finance API to fetch historical stock data.
   - Processes stock data for analysis and model training.

2. **Data Analysis**:
   - Performs exploratory data analysis (EDA) with descriptive statistics and visualizations.
   - Plots key metrics like adjusted close price, moving averages, and percentage changes.

3. **Model Development**:
   - Constructs an LSTM-based model using TensorFlow/Keras.
   - Implements data normalization and sliding window mechanisms for time-series data preparation.

4. **Visualization**:
   - Provides comparative plots for original vs. predicted prices.
   - Includes visualizations of stock trends and moving averages.

5. **Performance Evaluation**:
   - Calculates the Root Mean Square Error (RMSE) to evaluate model accuracy.
   - Offers insights into model predictions and real stock price trends.

---

## Dataset

The dataset comprises 20 years of historical stock data for Google (GOOG) obtained from the Yahoo Finance API. The key features include:

- **Open**: Opening price of the stock.
- **High**: Highest price of the stock during the trading session.
- **Low**: Lowest price of the stock during the trading session.
- **Close**: Closing price of the stock.
- **Adj Close**: Adjusted closing price accounting for splits and dividends.
- **Volume**: Number of shares traded.

---

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/stock-price-prediction-lstm.git
   cd stock-price-prediction-lstm
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Ensure you have Python 3.8+ installed.

---

## Usage

1. **Fetch Data**:
   Run the script to download and preprocess stock data:
   ```bash
   python data_preprocessing.py
   ```

2. **Train the Model**:
   Execute the training script to build the LSTM model:
   ```bash
   python train_model.py
   ```

3. **Visualize Results**:
   Analyze the predictions and original stock prices:
   ```bash
   python plot_results.py
   ```

---

## Model Architecture

The LSTM model consists of:

- Input layer for time-series data (100 timesteps).
- Two LSTM layers:
  - First LSTM layer with 128 units and return sequences enabled.
  - Second LSTM layer with 64 units and no return sequences.
- Dense layers for output:
  - One Dense layer with 25 units.
  - Final Dense layer with 1 unit to predict the next stock price.

Optimizer: Adam  
Loss Function: Mean Squared Error (MSE)

---

## Results

- The model achieved an RMSE of **3.76** on the test dataset.
- Visualizations highlight the alignment between predicted and actual stock prices, showcasing the effectiveness of the LSTM model.

---

## Contributions

Contributions are welcome! To contribute:

1. Fork this repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-branch
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add new feature"
   ```
4. Push to the branch:
   ```bash
   git push origin feature-branch
   ```
5. Open a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
