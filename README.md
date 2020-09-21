# LSTM Stock Predictor

![deep-learning.jpg](Images/deep-learning.jpg)

This repository contains the Unit 14 Deep Learning homework assigned. 

## Table of Contents

* Project Objective
* Project Conclusions
* Installation Requirements
* File Contents

### Project Objectives

* Build and evaluate deep learning models using both the Crypto Fear and Greed Index (FNG) and simple closing prices to determine if the FNG indicator provides a better signal for cryptocurrencies than the normal closing price data. 
    * Prepare data for training & testins
    * Build and train custom LSTM RRNs 

* Use deep learning recurrent neural networks to model bitcoin closing prices.

* Required to create two models: (1) Model 1 - using FNG indicators to predict closing price and (2) Model 2- use a window of closing prices to predict the following closing price

### Project Conclusions

(1) Which model has a lower loss?

Model loss with FNG values: loss: 0.1078 
Model loss with closing price: 0.0338

Based on our model evaluation, the model performed better with the closing price values.

(2) Which model tracks the actual values better over time?

Prediction vs Actual Graph using FNG values

![lstm_stock_predictor_fng.jpg](Images/lstm_stock_predictor_fng.jpg)

Prediction vs Actual Graph using closing prices

![lstm_stock_predictor_closing.jpg](Images/lstm_stock_predictor_closing.jpg)

Although the predicted values were slightly lower than the actual values with the closing-model, the difference between the two numbers was much less than the results received with the FNG-model. The average difference with the closing-model is showing ~1 compared to the fng-model where the average difference between predicted/actual is ~10.

With a lower difference in values of predicted and actual values, the model using the closing prices performed better than the model using FNG values. 

(3) Which window size works best for the model? 

FNG values model - 

Changes to window size did not lead to significant change to loss ~0.001 lower. 
The model performed relatively the same with different windown sizes.

Closing prices model - 

Changes to window size from 10 to 7 did lead to significant change in loss ~0.01 decrease.
The model perfermance varied between window sizes indicating multiple tests must occur with various window sizes to determine the optimal choice. 

