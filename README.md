# Stock Price Prediction with Bidirectional LSTM and Stacked LSTM

This README demonstrates the use of Bidirectional LSTM and Stacked LSTM neural networks for predicting stock prices using historical data.

## Dataset

- The dataset is loaded from the file `prices-split-adjusted.csv`.
- It contains historical stock prices including open, close, low, high, and volume.

## Preprocessing

- Features including open, close, low, high, and volume are selected from the dataset.
- Min-max scaling is applied to normalize the data between 0 and 1.
- Sequences of data with a window size of 10 are created, where each sequence represents historical data points.
- The target variable consists of the next data point after each sequence.

## Model Architecture

- The model consists of a Bidirectional LSTM layer followed by a Stacked LSTM layer and a Dense layer with the number of features as the output dimension.
- Dropout layers with a dropout rate of 0.2 are added to prevent overfitting.

## Training

- The dataset is split into training and testing sets with a test size of 20%.
- The model is trained for 10 epochs with a batch size of 32 and a validation split of 20%.

## Evaluation

- The model's performance is evaluated on the test set using the mean squared error (MSE) metric.

## Visualization

- Actual and predicted stock prices are plotted against time to visualize the model's performance.

## Dependencies

- pandas
- numpy
- scikit-learn
- TensorFlow
- matplotlib
