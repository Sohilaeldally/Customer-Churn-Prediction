# Customer Churn Prediction

![Alt text](https://daxg39y63pxwu.cloudfront.net/images/blog/churn-models/Customer_Churn_Prediction_Models_in_Machine_Learning.png)

## Project Overview
This project develops a machine learning model to predict customer churn for a telecommunications company. By analyzing customer data, the model identifies patterns that indicate whether a customer is likely to discontinue their service. The notebook `Churn Prediction.ipynb` implements data preprocessing, feature engineering, model training, and evaluation to achieve this goal.

## Dataset
The dataset is sourced from two CSV files:
- **churn-bigml-80.csv**: Training data (80% of the dataset, 2666 entries).
- **churn-bigml-20.csv**: Test data (20% of the dataset).

### Features
The dataset includes 20 columns:
- **Categorical Features**: `State`, `Area code`, `International plan`, `Voice mail plan`.
- **Numerical Features**: `Account length`, `Number vmail messages`, `Total day minutes`, `Total day calls`, `Total day charge`, `Total eve minutes`, `Total eve calls`, `Total eve charge`, `Total night minutes`, `Total night calls`, `Total night charge`, `Total intl minutes`, `Total intl calls`, `Total intl charge`, `Customer service calls`.
- **Target Variable**: `Churn` (boolean, True/False indicating whether the customer churned).

## Dependencies
To run the notebook, ensure you have the following Python libraries installed:
```bash
pip install -r requirements.txt
