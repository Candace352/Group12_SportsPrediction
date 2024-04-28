# Sports Prediction Model Deployment

This repository contains code for a sports prediction model developed using Jupyter Notebook in Google Colab. The model predicts player ratings based on various attributes.

## Getting Started

To get started with this project, follow these steps:

1. Clone this repository to your local machine.
2. Open the Jupyter Notebook file `Group12_SportsPrediction.ipynb` in Google Colab or any Jupyter Notebook environment.

## Data Preparation and Preprocessing

The notebook begins with data preparation and preprocessing steps:

- **Mounting Google Drive**: Mounting Google Drive to access the dataset stored in Google Drive.
- **Loading the Dataset**: Loading the dataset `players_21.csv` from Google Drive into a Pandas DataFrame.
- **Data Cleaning**: Removing columns with a high percentage of missing values and irrelevant columns like URLs, player pictures, etc.
- **Imputing Missing Values**: Imputing missing values in numerical columns using the mean and categorical columns using the mode.
- **Feature Scaling**: Scaling the numerical columns using StandardScaler.
- **Feature Encoding**: Encoding categorical columns using LabelEncoder.

## Feature Engineering

Feature engineering involves selecting highly correlated features with the target variable (`overall` player rating) to improve model performance.

## Training Models and Evaluation

The notebook trains multiple regression models including RandomForestRegressor, XGBRegressor, and GradientBoostingRegressor. The models are evaluated using mean absolute error (MAE) and mean squared error (MSE).

## Test with New Dataset

The trained model is tested with a new dataset `players_22.csv`. The new dataset undergoes the same preprocessing steps as the training dataset, and the optimized XGBRegressor model is used for prediction.

## Deployment Part 1

The trained models are saved using pickle for future deployment. Additionally, the StandardScaler object used for scaling the features is saved using joblib.

## Requirements

- Python 3
- Jupyter Notebook
- Required Python libraries (Pandas, NumPy, Scikit-learn, XGBoost, joblib)

## Important Links
Demonstration Video: https://drive.google.com/file/d/1eJfRgwqafL2AxYITxnGdiiIoSPOmvGHU/view?usp=sharing
Application Link: https://player-ratingapp.streamlit.app


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
