# House Price Prediction Using Linear Regression

## Overview
This project uses linear regression to predict house prices based on house attributes like area, bedrooms, bathrooms, etc. It demonstrates feature engineering, data preprocessing, and model building in Python.

## Dataset Description
The dataset contains these features:

- **price**: Target variable, house price
- **area**: Total house area (sq ft)
- **bedrooms**: Number of bedrooms
- **bathrooms**: Number of bathrooms
- **stories**: Number of floors
- **mainroad**: Access to main road (Yes/No)
- **guestroom**: Guest room availability (Yes/No)
- **basement**: Basement presence (Yes/No)
- **hotwaterheating**: Hot water heating availability (Yes/No)
- **airconditioning**: Air conditioning availability (Yes/No)
- **parking**: Number of parking spots
- **prefarea**: Preferred area location (Yes/No)
- **furnishingstatus**: Furnishing status (Furnished / Semi-furnished / Unfurnished)
- Engineered features like `areaperbedroom` and `bbratio` for better predictions.

## Data Preprocessing
- Converted categorical variables (like Yes/No) to binary 0/1.
- Created dummy variables for furnishing status.
- Added features based on domain knowledge.

## Model Building
- Used Scikit-learn’s LinearRegression model.
- Split data into training and test sets (optional).
- Trained and evaluated the model using R² and RMSE metrics.
