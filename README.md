# Stock_prediction_model_using_lstm

This code performs time series analysis and forecasting using a Long Short-Term Memory (LSTM) neural network on Apple (AAPL) stock prices. Here's a summary of the code:

1. **Data Retrieval:** Stock price data for AAPL is obtained using the Tiingo API through the `pandas_datareader` library. The data is then saved to a CSV file.

2. **Data Preprocessing:** The CSV file is loaded into a Pandas DataFrame, and the 'close' column is selected for further analysis. The data is normalized using Min-Max scaling.

3. **Time Series Dataset Creation:** The time series data is prepared by creating input sequences (`X_train` and `X_test`) and corresponding output values (`y_train` and `y_test`) with a specified time step.

4. **LSTM Model Architecture:** A sequential LSTM model is defined with three LSTM layers and one dense layer. The model is compiled using the mean squared error loss function and the Adam optimizer.

5. **Model Training:** The model is trained using the training data (`X_train` and `y_train`) for 100 epochs with a batch size of 64.

6. **Model Evaluation:** The trained model is used to make predictions on both the training and testing datasets. The predictions are then inverse-transformed to the original scale for evaluation using the root mean squared error (RMSE).

7. **Plotting Results:** The training and testing predictions are plotted against the actual stock prices, providing a visual representation of the model's performance.

8. **Future Price Prediction:** The code includes a loop to predict future stock prices for the next 30 days. The predicted values are appended to the input sequence iteratively, and the process is repeated.

9. **Visualization of Future Predictions:** The future predictions are plotted alongside the existing data, showing the continuation of the time series.
