# Car Price Prediction Using Machine Learning

This repository contains a machine learning project that predicts used car prices based on various features such as brand, engine capacity, fuel type, and more. The project compares the performance of three regression models: **Linear Regression**, **Decision Tree Regressor**, and **Random Forest Regressor**.

## 📁 Dataset

The dataset used for this project is `car details v4.csv`, which includes various attributes of used cars such as:
- Make (Brand)
- Year
- Engine
- Transmission
- Fuel Type
- Owner Type
- Seller Type
- Drivetrain
- Seating Capacity
- Fuel Tank Capacity
- Price (Target variable)

The dataset is fetched using `gdown` from a Google Drive link.

## 📊 Features Engineering & Cleaning

- Dropped unnecessary columns such as: `Model`, `Max Power`, `Max Torque`, `Length`, `Width`, `Height`, `Color`, `Kilometer`.
- Handled missing values by removing rows with `NaN`s.
- Engine column cleaned (removed 'cc' and converted to integers).
- Scaled `Price` using `MinMaxScaler`.
- Categorical variables encoded using one-hot encoding (`get_dummies()`).
- Added a custom column `Condition` with random categories for demo/testing purposes.

## 🧠 Models Used

1. **Linear Regression**
2. **Decision Tree Regressor**
3. **Random Forest Regressor**

Each model is evaluated using:
- R² Score
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- Root Mean Squared Logarithmic Error (RMSLE)

Cross-validation (`K=10`) is used to evaluate generalization performance.

## 📈 Evaluation Metrics

- **R² Score**: Measures how well predictions approximate actual values.
- **RMSE**: Penalizes large errors more heavily.
- **MAE**: Measures average magnitude of the errors.
- **RMSLE**: Useful when predicting variables that grow exponentially (like price).

## 📉 Visualizations

- Scatter plots showing predicted prices vs. actual prices for both training and test sets for each model.

## 🧪 Requirements

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn gdown
