Linear Regression

## Objective
[cite_start]The goal of this task was to implement and understand both simple and multiple linear regression models using a house price prediction dataset[cite: 2, 13].

## Tools Used
* [cite_start]**Scikit-learn (sklearn):** For building and evaluating the linear regression models[cite: 6].
* [cite_start]**Pandas:** For importing, handling, and preprocessing the dataset[cite: 6].
* [cite_start]**Matplotlib:** For visualizing the results, such as the regression line and the model's predictions[cite: 6].

---

## Steps Taken

### 1. Data Preprocessing
* [cite_start]The `Housing.csv` dataset was loaded into a pandas DataFrame[cite: 8].
* Binary categorical features like `mainroad`, `guestroom`, and `airconditioning` were mapped to numerical values (1 for 'yes', 0 for 'no') to prepare them for the model.
* The `furnishingstatus` feature, which has multiple categories, was converted into numerical format using one-hot encoding. This created new columns like `semi-furnished` and `unfurnished`. To avoid multicollinearity, one of the dummy variables (`furnished`) was dropped.
* Two new features were engineered: `areaperbedroom` (area divided by bedrooms) and `bbratio` (bathrooms divided by bedrooms).

### 2. Simple Linear Regression
* [cite_start]A simple linear regression model was built using `area` as the independent variable (`X_simple`) to predict `price` (the dependent variable `y`)[cite: 24, 25, 26].
* [cite_start]The data was split into a training set and a testing set (80/20 split) to ensure the model's performance could be evaluated on unseen data[cite: 9, 25].
* [cite_start]The model was trained on the training data[cite: 10, 26].
* [cite_start]Predictions were made on the test set[cite: 27].
* [cite_start]The model was evaluated using Mean Absolute Error (MAE), Mean Squared Error (MSE), and the $R^2$ score[cite: 11, 28].
* [cite_start]The model's coefficients and intercept were printed for interpretation[cite: 28].
* [cite_start]A scatter plot was created to visualize the regression line against the actual prices[cite: 12, 29].

### 3. Multiple Linear Regression
* [cite_start]A multiple linear regression model was implemented using all preprocessed features (e.g., `area`, `bedrooms`, `bathrooms`, `stories`, `airconditioning`, `semi-furnished`, etc.) to predict `price`[cite: 22, 32].
* [cite_start]The data was split into training and testing sets[cite: 33].
* [cite_start]The model was trained on the training data[cite: 10, 34].
* [cite_start]Predictions were made on the test set[cite: 35].
* [cite_start]The model was evaluated using MAE, MSE, and the $R^2$ score[cite: 11, 40].
* [cite_start]The intercept and coefficients for all independent variables were printed to show their impact on the predicted house price[cite: 12, 42].
* [cite_start]A plot of the actual prices versus the predicted prices was generated to visualize the model's performance[cite: 39].

---

## Conclusion
The multiple linear regression model performed significantly better than the simple linear regression model, as indicated by its higher $R^2$ score and lower MAE and MSE values. This demonstrates that house prices are influenced by multiple factors, not just one single variable like area. The coefficients of the multiple regression model provide valuable insights into which features have the greatest positive or negative impact on the predicted price.
