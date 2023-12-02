# Energy Output Prediction with Neural Networks

This project uses a neural network to predict energy output based on ambient temperature, exhaust vacuum, ambient pressure, and relative humidity. The dataset used is "Folds5x2_pp.xlsx."

## Requirements

Make sure you have the following dependencies installed:

- pandas
- numpy
- scikit-learn
- tensorflow

## Models

The project includes the following models:

- **Model_1**: Basic neural network with one hidden layer.
- **Model_2_1, Model_2_2, Model_2_3**: Optimized versions of Model_2 with additional layers and increased training epochs.

## Results

The project compares the performance of different models based on Mean Absolute Error (MAE) and Mean Squared Error (MSE). Model_2_1 is identified as the best-performing model.

### Evaluation Results

| Model     | MAE       | MSE       |
|-----------|-----------|-----------|
| Model_1   | mae_v1    | mse_v1    |
| Model_2   | mae_v2    | mse_v2    |
| Model_3   | mae_v3    | mse_v3    |
| Model_2_1 | mae_v2_1  | mse_v2_1  |
| Model_2_2 | mae_v2_2  | mse_v2_2  |
| Model_2_3 | mae_v2_3  | mse_v2_3  |

### Prediction Comparison

A DataFrame (`con_df`) is provided, comparing the predictions of different models against the actual `y_test` values.

## Saving the Best Model

The best-performing model (Model_2_1) is saved for future use:

```bash
model.save("Best_model")
```

You can load the model using:

```python
best_model = tf.keras.models.load_model("Best_model")
```
