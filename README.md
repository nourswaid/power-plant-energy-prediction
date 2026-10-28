# Artificial Neural Network (ANN) for Regression

## Project Overview

This project implements an Artificial Neural Network (ANN) using TensorFlow and Keras to solve a regression problem. The model predicts electrical energy output using the **Combined Cycle Power Plant dataset** (`Folds5x2_pp.xlsx`).

The objective is to build, train, and evaluate a neural network for predicting continuous numerical values.

## Dataset

The dataset contains measurements from a combined cycle power plant.

**Input features:**
- `AT` — Ambient Temperature
- `V` — Exhaust Vacuum
- `AP` — Ambient Pressure
- `RH` — Relative Humidity

**Target variable:**
- `PE` — Net hourly electrical energy output

## Model Architecture

The ANN is built using TensorFlow and Keras with the following architecture:

- **Input layer:** Receives the four input features.
- **Hidden layer 1:** 6 neurons with ReLU activation.
- **Hidden layer 2:** 6 neurons with ReLU activation.
- **Output layer:** 1 neuron for regression prediction.

## Model Configuration

- **Framework:** TensorFlow / Keras
- **Optimizer:** Adam
- **Loss function:** Mean Squared Error (MSE)
- **Epochs:** 100
- **Batch size:** 32
- **Train-test split:** 80% training, 20% testing
- **Random state:** 0

## Model Evaluation

The model is evaluated using three regression metrics:

- **R² Score:** Measures how well the model explains the variation in the target variable. A score closer to 1 generally indicates a better fit.
- **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and predicted values.
- **Root Mean Squared Error (RMSE):** Measures the square root of the average squared prediction errors, penalizing larger errors more heavily.

These metrics provide different perspectives on the model's predictive performance.

## Technologies Used

- Python
- TensorFlow / Keras
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook / Google Colab

## How to Run

1. Clone or download this repository.
2. Install the required libraries:

   ```bash
   pip install tensorflow pandas numpy scikit-learn openpyxl
   ```

3. Make sure `Folds5x2_pp.xlsx` is available at the dataset path specified in the notebook. If running in Google Colab, upload the file to the appropriate location.
4. Open and run `Artificial_Neural_Network.ipynb`.
5. Review the model's predictions and evaluation metrics.

## Future Improvements

Possible extensions include:
- Visualizing training loss across epochs.
- Applying feature scaling and evaluating its effect on performance.
- Experimenting with different network architectures and hyperparameters.

## Author

Developed as a Data Science project to practice implementing and evaluating an ANN for regression using TensorFlow and Keras.
