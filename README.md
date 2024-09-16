# Time-Series-Transformer-Oil-Temp-Forecast
Time series forecasting assignment to predict electricity transformer oil temperature for the next 24 hours using machine learning models (LSTM). Includes data preprocessing, feature engineering, model evaluation, and documentation for project structure and dependencies.

## Project Overview
This project aims to forecast the oil temperature (OT) of electricity transformers on an hourly basis using historical data. The prediction is crucial for managing transformer loads and preventing damage.

### Problem Context
Accurately predicting oil temperature helps in preventing equipment failures and optimizing energy distribution.

## Data
The data provided contains the following columns:
- **date**: Date of observation
- **HUFL**: High Useful Load
- **HULL**: High Useless Load
- **MUFL**: Middle Useful Load
- **MULL**: Middle Useless Load
- **LUFL**: Low Useful Load
- **LULL**: Low Useless Load
- **OT**: Oil Temperature (Target)

### Data Preprocessing
- Missing values were handled, and the data was scaled using `StandardScaler`.
- Feature engineering was performed by creating time-related features such as hour, day, month, and weekday.

### Feature Engineering
New features such as lag variables and rolling means were created to capture time-dependent patterns in the data.

### Model
A Long Short-Term Memory (LSTM) neural network was built to model the time-series data and forecast OT for the next 24 hours.

### Evaluation Metrics
The model was evaluated using the following metrics:
- **MAE** (Mean Absolute Error)
- **RMSE** (Root Mean Squared Error)
- **MAPE** (Mean Absolute Percentage Error)

## Assumptions

1. The datasets `train.csv` and `test.csv` contain columns `HUFL`, `HULL`, `MUFL`, `MULL`, `LUFL`, `LULL`, `OT`, and `date`.
2. The target variable for prediction is `OT` (Oil Temperature).
3. Time-series forecasting is done using LSTM, which requires the input to be reshaped as (samples, timesteps, features).

## Project Structure
/project-directory │ ├── train.csv # Training dataset ├── test.csv # Test dataset ├── Forecast_OT.ipynb # Jupyter Notebook containing code ├── README.md # Project documentation (this file) # Dependencies


### Dependencies
- pandas
- numpy
- scikit-learn
- tensorflow
- matplotlib
- seaborn
- plotly

## Usage

1. Clone the repository.
2. Install dependencies (given).
3. Load the files into Jupyter notebook/ Google Colab.
4. Place the `train.csv` and `test.csv` files in the same folder as Forecast_OT.ipynb.
5. Run all the cells in file Forecast_OT.ipynb to load the data, build the model, and generate predictions.
