# FINTECH_Project_2
## Resources 


Boosted LSTM Integration 
### Implementation of Code for Training an initial LSTM Model on a dataset 

Base Model Training:

Begin by training an initial LSTM model on the dataset.
Compute the residuals or errors (difference between the predicted and actual values).
Sequential Training:

Train additional LSTM models on the residuals of the previous models.
Each model focuses on learning the patterns missed by its predecessors.
Aggregation of Predictions:

Combine the predictions of all LSTM models, typically by weighted averaging, where weights can be determined based on the performance of each model on a validation dataset.
Model Complexity:

Carefully choose the complexity of each LSTM in the ensemble. Too complex models might overfit, especially in later stages where the focus is on fitting residuals.
Learning Rate Adjustments:

Adjust the learning rates for each subsequent LSTM. Later models might benefit from lower learning rates to fine-tune the predictions on residuals.
Regularization Techniques:

Use dropout, recurrent dropout, and possibly L1/L2 regularization to prevent overfitting, especially since boosting can increase the risk of overfitting by focusing too narrowly on specific aspects of the dataset.
Early Stopping:

Implement early stopping during training of each LSTM model to avoid overfitting on noise in the residuals.
Error Monitoring:

Continuously monitor the error patterns; if subsequent models do not significantly improve the predictions, consider stopping the addition of new models to the ensemble.
Diverse Initialization:

Initialize each LSTM model differently to promote model diversity, which is key to the success of ensemble methods.


### Imports

import numpy as np
import tensorflow as tf
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error

# Step 1: Prepare your dataset
# Assuming you have your dataset prepared with features X and labels y
# Split the data into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Step 2: Base Model Training
# Build and train the initial LSTM model
model = tf.keras.Sequential([
    tf.keras.layers.LSTM(units=64, input_shape=(X_train.shape[1], X_train.shape[2])),
    tf.keras.layers.Dense(1)
])
model.compile(optimizer='adam', loss='mse')
model.fit(X_train, y_train, epochs=10, batch_size=32, validation_split=0.1)

# Step 3: Compute Residuals
# Predict on the training data to compute residuals
y_pred_train = model.predict(X_train)
residuals = y_train - y_pred_train

# Step 4: Sequential Training
# Train additional LSTM models on the residuals
num_boosting_rounds = 5
boosted_models = []
for i in range(num_boosting_rounds):
    boosted_model = tf.keras.Sequential([
        tf.keras.layers.LSTM(units=64, input_shape=(X_train.shape[1], X_train.shape[2])),
        tf.keras.layers.Dense(1)
    ])
    boosted_model.compile(optimizer='adam', loss='mse')
    boosted_model.fit(X_train, residuals, epochs=5, batch_size=32, validation_split=0.1)
    boosted_models.append(boosted_model)
    # Compute new residuals for the next iteration
    residuals = y_train - np.sum([model.predict(X_train) for model in boosted_models], axis=0)

# Step 5: Aggregation of Predictions
# Combine predictions of all LSTM models by weighted averaging
def predict_boosted(X, models, weights=None):
    if weights is None:
        weights = np.ones(len(models)) / len(models)
    predictions = [model.predict(X) * weight for model, weight in zip(models, weights)]
    return np.sum(predictions, axis=0)

# Step 6: Model Complexity, Learning Rate Adjustments, Regularization Techniques, Early Stopping
# These can be implemented by adjusting model hyperparameters and training procedures accordingly

# Step 7: Evaluate the boosted model
y_pred_test = predict_boosted(X_test, boosted_models)
mse = mean_squared_error(y_test, y_pred_test)
print("Mean Squared Error on Test Set:", mse)




https://app.intotheblock.com/coin/BTC

https://bitcoinvisuals.com/

https://defillama.com/docs/api

https://fred.stlouisfed.org/docs/api/fred/#API

https://stocktoflow.com/

https://developer.twitter.com/en/docs/api-reference-index

