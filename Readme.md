# ﻿**🌦️ Time Series Forecasting & Anomaly Detection with VAE & GRU**

# **📌 Project Overview**

This project implements **Time Series Forecasting** and **Anomaly Detection** on weather data using:

- **Variational Autoencoder (VAE)** for detecting anomalies in weather patterns.
- **Gated Recurrent Unit (GRU)** for predicting future weather conditions.

The dataset used is the **Hourly Weather Surface - Brazil** dataset, containing temperature, humidity, wind speed, and other atmospheric conditions.

# **📊 Dataset**

**Source**: Kaggle - Hourly Weather Surface, Brazil

# **🔹 Data Preprocessing**

- Exploratory Data Analysis (EDA): Visualizing feature distributions, time series plots.
- Handling missing values and outliers.
- Normalizing/standardizing data.
- Creating sequences for time series forecasting.
- Splitting into training, validation, and test sets.

# **🛠️ Implementation Steps**

# **Part 1: VAE for Anomaly Detection**

✅ **Model Architecture**

- Encoder with **2+ hidden layers**
- Latent space with a tunable dimension
- Decoder with **2+ hidden layers**
- Proper sampling using a reparameterization trick

✅ **Training**

- Loss function: **Reconstruction Loss + KL Divergence**
- Implement **Early Stopping**
- Monitor training with loss curves

✅ **Anomaly Detection**

- Define **anomaly score** based on reconstruction error
- Detect unusual weather days (e.g., extreme temperature changes)
- Evaluate using **Precision, Recall, F1-score**
- Experiment with different anomaly thresholds

✅ **Latent Space Analysis**

- Visualize the latent space
- Generate synthetic weather patterns by sampling from latent space

**Part 2: GRU for Time Series Forecasting**

✅ **Model Architecture**

- GRU-based network with multiple weather features as inputs
- At least **one GRU layer** with an optimized number of units
- Appropriate output layer for sequence forecasting

✅ **Training**

- Uses past **N hours** to predict **M future hours**
- Implements **Teacher Forcing** with a decay schedule
- Uses **batch training** and **learning rate scheduling**
- Monitors training loss (MSE, MAE, RMSE)

✅ **Evaluation & Performance Metrics**

- Computes **MSE, MAE, RMSE** on test data
- Visualizes **Predictions vs. Actual Values**
- Analyzes how far into the future the model can predict accurately

**Part 3: Model Integration**

✅ **Combining VAE & GRU**

- Uses **VAE** for anomaly detection in input data
- Evaluates **GRU performance on normal vs. anomalous data**

# **📌 Results & Insights**

- Effectiveness of **VAE in anomaly detection**
- **Performance comparison** of GRU vs. LSTM vs. RNN
- Impact of sequence length and feature selection on forecasting
- **Visualizations of anomalies and forecasting results**

