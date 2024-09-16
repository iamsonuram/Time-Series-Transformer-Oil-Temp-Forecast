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
- Data is assumed to be correctly preprocessed.
- StandardScaler and MinMaxScaler are used for feature scaling.
- No pre-trained models were used, as per the project guidelines.

## Project Structure
/project-directory │ ├── train.csv # Training dataset ├── test.csv # Test dataset ├── forecast.ipynb # Jupyter Notebook containing code ├── README.md # Project documentation (this file) ├── requirements.txt # Dependencies


### Dependencies
- pandas
- numpy
- scikit-learn
- tensorflow
- matplotlib
- seaborn
- plotly
