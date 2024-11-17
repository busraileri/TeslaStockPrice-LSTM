# TeslaStockPrice-LSTM
This project utilizes Long Short-Term Memory (LSTM), a type of Recurrent Neural Network (RNN), to predict Tesla's stock prices based on historical data. 


## Project Overview
Stock market prediction is a challenging task due to the stochastic nature of stock prices. This project focuses on predicting Tesla's stock prices using LSTM to analyze sequential data and capture time-based patterns effectively.

---

## Dataset
The dataset contains Tesla's stock data from June 29, 2010, to February 3, 2020.  
### Features:
- **Date**: Trading day.
- **Open**: Opening price of the stock.
- **High**: Highest price of the stock.
- **Low**: Lowest price of the stock.
- **Close**: Closing price of the stock.
- **Adj Close**: Adjusted closing price.
- **Volume**: Trading volume.

Dataset Source: [Kaggle - Tesla Stock Data (2010–2020)](https://www.kaggle.com/datasets)

---

**Data Preprocessing**
- Loading the Data: The dataset is loaded using pandas.
- Feature Selection: Only the "Close" price is used for prediction.
- Scaling: MinMaxScaler is applied to normalize the data between 0 and 1.
- Train-Test Split: Data is split into 80% training and 20% testing sets.
- Feature Creation: A sliding window (lookback) approach is used to create input-output pairs.

**Model Architecture**

The LSTM model is implemented using TensorFlow's Keras API with the following structure:
- LSTM Layers: To capture time-series dependencies.
- Dense Layers: For output prediction.
- Dropout: To prevent overfitting.

**Training and Evaluation**
- Loss Function: Mean Squared Error (MSE) is used.
- Optimizer: Adam optimizer.
- Metrics: MSE and RMSE are computed to evaluate model performance.
- Callbacks: Early stopping and model checkpointing are used to improve training efficiency.


## Libraries
```bash
numpy
pandas
tensorflow
matplotlib
scikit-learn
```
