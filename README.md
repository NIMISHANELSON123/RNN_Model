# RNN_Model
# Weather Forecasting using Simple RNN

This project is a simple implementation of a Recurrent Neural Network (RNN) using TensorFlow and Keras to predict future weather temperatures based on historical weather data (`weatherHistory.csv`).

## Project Structure

The project is structured into three main parts:

- **Part A: Data Understanding and Preprocessing**
  - Loaded the weather dataset and checked the first few rows.
  - Handled missing values using forward fill (`ffill`).
  - Normalized the dataset using `MinMaxScaler` to help the RNN converge faster.
  - Created input sequences using past weather data (temperature, humidity, wind speed) to predict the next day's temperature.
  - Split the dataset into training, validation, and testing sets.

- **Part B: RNN Model Development**
  - Built a Sequential model with a `SimpleRNN` layer (50 units, ReLU activation) and a `Dense` output layer.
  - Compiled the model using the Adam optimizer, Mean Squared Error (MSE) loss, and Mean Absolute Error (MAE) metric.
  - Trained the model using a batch size of 32 for 50 epochs while monitoring performance with validation data.
  - Visualized the training versus validation loss curves to check model learning and prevent overfitting.

- **Part C: Model Evaluation & Forecasting**
  - Evaluated the trained model on the test dataset using metrics like RMSE, MAE, and $R^2$ score.
  - Plotted a comparison graph of predicted versus actual temperatures for the test period.
  - Implemented a recursive forecasting function to predict the next 7 days of temperature and visualized the results alongside recent historical data.

## Requirements

- Python 3.x
- TensorFlow / Keras
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
