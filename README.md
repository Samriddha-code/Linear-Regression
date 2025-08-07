Linear Regression

## Objective
The goal of this task was to implement and understand both simple and multiple linear regression models using a house price prediction dataset.

## Tools Used
**Scikit-learn (sklearn):** For building and evaluating the linear regression models.
**Pandas:** For importing, handling, and preprocessing the dataset.
**Matplotlib:** For visualizing the results, such as the regression line and the model's predictions.

---

## Steps Taken

### 1. Data Preprocessing
*The `Housing.csv` dataset was loaded into a pandas DataFrame.
* Binary categorical features like `mainroad`, `guestroom`, and `airconditioning` were mapped to numerical values (1 for 'yes', 0 for 'no') to prepare them for the model.
* The `furnishingstatus` feature, which has multiple categories, was converted into numerical format using one-hot encoding. This created new columns like `semi-furnished` and `unfurnished`. To avoid multicollinearity, one of the dummy variables (`furnished`) was dropped.
* Two new features were engineered: `areaperbedroom` (area divided by bedrooms) and `bbratio` (bathrooms divided by bedrooms).

### 2. Simple Linear Regression
*A simple linear regression model was built using `area` as the independent variable (`X_simple`) to predict `price` (the dependent variable `y`).
*The data was split into a training set and a testing set (80/20 split) to ensure the model's performance could be evaluated on unseen data.
*The model was trained on the training data.
*Predictions were made on the test set.
*The model was evaluated using Mean Absolute Error (MAE), Mean Squared Error (MSE), and the $R^2$ score.
*The model's coefficients and intercept were printed for interpretation.
*A scatter plot was created to visualize the regression line against the actual prices.

### 3. Multiple Linear Regression
*A multiple linear regression model was implemented using all preprocessed features (e.g., `area`, `bedrooms`, `bathrooms`, `stories`, `airconditioning`, `semi-furnished`, etc.) to predict `price`.
*The data was split into training and testing sets.
*The model was trained on the training data.
*Predictions were made on the test set.
*The model was evaluated using MAE, MSE, and the $R^2$ score.
*The intercept and coefficients for all independent variables were printed to show their impact on the predicted house price.
*A plot of the actual prices versus the predicted prices was generated to visualize the model's performance.

---

## Conclusion
The multiple linear regression model performed significantly better than the simple linear regression model, as indicated by its higher $R^2$ score and lower MAE and MSE values. This demonstrates that house prices are influenced by multiple factors, not just one single variable like area. The coefficients of the multiple regression model provide valuable insights into which features have the greatest positive or negative impact on the predicted price.
