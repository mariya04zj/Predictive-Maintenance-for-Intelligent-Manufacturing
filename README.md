
The Industry 4.0 has encouraged smart manufacturing of products through real-time monitoring of industrial
machines via IoT sensors and 6G networks. This dataset captures critical metrics like power consumption,
vibration and a target variable of predictive maintenance scores. Time series analysis helps to uncover
patterns in machine behavior, detect anomalies and forecast maintenance needs. By modeling trends,
seasonality, and sensor correlations, we can optimize eCiciency, reduce downtime and enhance predictive
maintenance strategies. This project uses and compares these techniques to find the model with the lowest MSE 
for better predictive maintenance by early detection of faults. The study concluded with an LSTM model.

The Long Short-Term Memory (LSTM) model is a specialized type of recurrent neural network (RNN)
designed to capture long-term dependencies and complex temporal patterns in sequential data.
Unlike traditional time series models, they excel at learning non-linear relationships and can handle
variable-length input sequences, making them ideal for forecasting tasks with irregular or noisy data.
In predictive maintenance, LSTMs process multivariate time series data like the IoT sensor readings
to predict equipment failures by recognizing subtle degradation patterns over time. The model retains
important information while discarding the irrelevant noise our data has. LSTMs work better when
combined with feature engineering like rolling statistics or lagged variables. They can integrate
exogenous inputs as additional features. Although computationally intensive, they are a powerful
tool for scenarios where traditional methods fall short, provided enough training data is available,
like in our case.

The model architecture consists of two LSTM layers: the first with 50 units and outputs pass to the
next layer in a sequential manner, followed by a 20% dropout for regularization, and a second LSTM
layer with 50 units to further process the temporal patterns. A dense output layer with one unit
generates the final prediction. The model is compiled using the Adam optimizer and mean squared
error loss, suitable for regression tasks. Training is done for 50 steps with a batch size of 16,
optimizing the network to minimize prediction error on the training data.

<img width="618" alt="Screenshot 2025-04-17 at 12 01 43 AM" src="https://github.com/user-attachments/assets/308b6ef8-2759-4a0e-bb4f-6ed909251047" />
