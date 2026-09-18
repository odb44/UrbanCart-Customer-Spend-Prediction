# UrbanCart-Customer-Spend-Prediction
Machine learning regression project for predicting UrbanCart customers' next-month spending using Linear Regression and Random Forest.

## Project Overview

This project focuses on predicting how much each UrbanCart customer will spend in the following month using machine learning regression models.

The project applies data exploration, feature selection, preprocessing, train-validation-test splitting, model training, and regression evaluation to develop a predictive solution.

## Business Objective

UrbanCart wants to estimate each customer's expected spending for the next month.

Accurate spending predictions can support business activities such as:

- Customer segmentation
- Sales forecasting
- Targeted marketing
- Customer planning and retention strategies

## Dataset

The dataset contains 20,000 customer records with the following variables:

| Feature | Description |
|---|---|
| `MonthsActive` | Number of months the customer has been active |
| `AvgOrderValue` | Average value of the customer's orders |
| `NumOrdersLastQuarter` | Number of orders placed during the last quarter |
| `Region` | Customer's geographical region |
| `NextMonthSpend` | Target variable representing predicted next-month spending |

## Machine Learning Approach

The project uses two regression approaches:

1. **Linear Regression** — used as a baseline model.
2. **Random Forest Regression** — used as a more flexible tree-based model capable of capturing nonlinear relationships.

The dataset was divided into:

- 64% Training
- 16% Validation
- 20% Testing

The validation set was used for model comparison, while the test set was used for final evaluation.

## Preprocessing

The categorical `Region` feature was transformed using one-hot encoding.

A Scikit-learn pipeline was used to combine preprocessing and model training, ensuring that the same transformations were consistently applied during training and prediction.

## Model Evaluation

The models were evaluated using:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

### Test Results

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 9.85 | 12.33 | 0.830 |
| Random Forest | 10.46 | 13.06 | 0.809 |

Linear Regression produced more consistent performance across the training, validation, and test sets. Random Forest achieved a substantially higher training performance but showed a larger gap between training and unseen-data performance, indicating overfitting.

## Recommendation

Based on the validation and test results, Linear Regression was selected as the model for predicting `NextMonthSpend`.

The model achieved a test R² of 0.830, meaning it explains approximately 83% of the variation in next-month customer spending in the test data.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Git
- GitHub

## Project Author

**Oluwaseun Bamigbele**
