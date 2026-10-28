 # Predicting Electrical Energy Output of a Combined Cycle Power Plant

## Project Overview

This project implements an Artificial Neural Network (ANN) using TensorFlow and Keras to predict the net electrical energy output of a Combined Cycle Power Plant based on environmental measurements.

The objective is to build, train, and evaluate a neural network for a regression task using real-world data.

## Dataset

This project uses the **Combined Cycle Power Plant** dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/294/combined%2Bcycle%2Bpower%2Bplant).

The dataset contains 9,568 observations collected over six years (2006–2011).

**Input features:**

| Feature | Description |
|---|---|
| `AT` | Ambient Temperature (°C) |
| `V` | Exhaust Vacuum (cm Hg) |
| `AP` | Ambient Pressure (millibar) |
| `RH` | Relative Humidity (%) |

**Target variable:**
- `PE` — Net hourly electrical energy output (MW)

### Dataset Citation

Tüfekci, P. & Kaya, H. (2014). *Combined Cycle Power Plant* [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5002N

## Model Architecture

The ANN was built using TensorFlow and Keras with the following architecture:

- **Input:** Four input features.
- **Hidden Layer 1:** 6 neurons with ReLU activation.
- **Hidden Layer 2:** 6 neurons with ReLU activation.
- **Output Layer:** 1 neuron for regression prediction.

## Model Configuration

| Parameter | Value |
|---|---|
| Framework | TensorFlow / Keras |
| Model type | Artificial Neural Network (ANN) |
| Task | Regression |
| Optimizer | Adam |
| Loss function | Mean Squared Error (MSE) |
| Epochs | 100 |
| Batch size | 32 |
| Training set | 80% |
| Test set | 20% |
| Random state | 0 |

## Model Evaluation

The model is evaluated using three regression metrics:

- **R² Score:** Measures how much of the variance in the target variable is explained by the model. A score closer to 1 generally indicates a better fit.
- **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and predicted values.
- **Root Mean Squared Error (RMSE):** Measures the square root of the average squared prediction errors, giving greater weight to larger errors.

## Technologies Used

- Python
- TensorFlow / Keras
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook / Google Colab

## How to Run

1. Clone this repository.
2. Install the required libraries:

   ```bash
   pip install tensorflow pandas numpy scikit-learn openpyxl
   ```

3. Download the `Folds5x2_pp.xlsx` dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/294/combined%2Bcycle%2Bpower%2Bplant).
4. Open `Artificial_Neural_Network.ipynb` in Jupyter Notebook or Google Colab.
5. **Update the dataset path** in the notebook to match where you saved the Excel file.

   For example, on a local computer:

   ```python
   dataset = pd.read_excel(r"C:\path\to\Folds5x2_pp.xlsx")
   ```

   Replace the example path with the actual location of your downloaded file.

   If you're using Google Colab, upload the dataset and use:

   ```python
   dataset = pd.read_excel('/content/Folds5x2_pp.xlsx')
   ```

6. Run the notebook cells to train the model, generate predictions, and evaluate its performance.

## Future Improvements

- Visualize training loss across epochs.
- Experiment with feature scaling and evaluate its effect on performance.
- Experiment with different network architectures and hyperparameters.

## Acknowledgments

The dataset was obtained from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/294/combined%2Bcycle%2Bpower%2Bplant). Credit goes to the original dataset creators, Pınar Tüfekci and Heysem Kaya.

## Author

Developed as a Data Science project to practice implementing and evaluating an Artificial Neural Network for regression using TensorFlow and Keras.
