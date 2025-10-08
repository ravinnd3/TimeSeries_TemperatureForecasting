Dataset - https://www.kaggle.com/datasets/paulbrabban/daily-minimum-temperatures-in-melbourne

[Temperature Forecasting PDF.pdf](https://github.com/user-attachments/files/22750807/Temperature.Forecasting.PDF.pdf)

1. Introduction
   
Accurate temperature forecasting is essential for agriculture, energy management, and climate analysis. With the advancement of data science and machine learning, both statistical and neural network-based models have become powerful tools for time series forecasting. This project aims to develop and evaluate multiple forecasting models using historical temperature data obtained from Kaggle, leveraging both classical and deep learning approaches.

2. Objective
   
The main objective of this project is to forecast future temperature values using various time series models and compare their performance. The study evaluates traditional statistical methods alongside advanced neural architectures and hybrid models to determine the most efficient forecasting technique.

3. Dataset
   
The dataset, sourced from Kaggle, contains historical daily temperature records over several years.
Extensive feature engineering was performed, including:
Date-based decomposition (year, month, day, seasonality features)
Rolling statistics (moving average, lag features)
Normalization/scaling of data for neural models
Handling missing values and ensuring stationarity where required

4. Models Implemented
   
   A. Statistical Models
   ARIMA (AutoRegressive Integrated Moving Average) – Captures trend and autoregressive dependencies.
   SARIMAX (Seasonal ARIMA with eXogenous variables) – Extends ARIMA to model seasonal patterns and external regressors.
   
   B. Deep Learning Models
   Simple RNN (Recurrent Neural Network) – Captures sequential dependencies in temperature data.
   Stacked RNN – Multiple RNN layers to model deeper temporal relationships.
   LSTM (Long Short-Term Memory) – Addresses vanishing gradient issues, capturing long-term dependencies.
   GRU (Gated Recurrent Unit) – Simplified variant of LSTM with similar performance.
   Bidirectional RNN – Considers dependencies in both forward and backward time directions.
   
   C. Hybrid Model
   CNN + RNN Hybrid – Combines Convolutional Neural Networks for feature extraction with RNN for temporal learning, improving pattern recognition and predictive accuracy.
   
   D. Probabilistic and Additive Models
   Prophet (Facebook) – Handles trend, seasonality, and holiday effects using an additive model.
   NeuralProphet – A neural network-based extension of Prophet, integrating autoregressive components and improved handling of non-linear trends.
   
5. Evaluation Metrics
   
   Model performance was compared using:
   RMSE (Root Mean Squared Error)
   MAE (Mean Absolute Error)
   R² Score (Coefficient of Determination)
   Visualization of forecasted vs actual temperature values
   
6. Results and Analysis
   
Each model was trained and tested on the processed dataset.
Comparative analysis was performed to identify:
The best-performing model for short-term and long-term forecasting.
The trade-offs between interpretability (Prophet/SARIMAX) and accuracy (Deep Learning/Hybrid).
Preliminary results indicate that deep learning and hybrid models outperform traditional statistical methods for complex, nonlinear patterns.

7. Conclusion
    
This study demonstrates that integrating both traditional time series models and deep learning architectures provides a robust framework for temperature forecasting. While SARIMAX and Prophet offer interpretability and stability, LSTM, GRU, and Hybrid (CNN+RNN) models deliver superior predictive accuracy by capturing complex temporal and spatial dependencies.
Future work includes hyperparameter optimization, inclusion of exogenous climatic variables (humidity, wind speed, etc.), and deployment of the best-performing model for real-time temperature prediction.
