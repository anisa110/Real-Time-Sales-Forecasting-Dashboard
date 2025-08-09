Real-Time Sales Forecasting using Prophet
Overview
This project implements a time-series forecasting model to predict future retail sales based on historical sales data. The dataset contains daily sales figures along with additional product, store, and category information. The forecasting model is built using the Prophet library, and performance is evaluated using standard error metrics.

Dataset
The dataset used in this project is retail_store_inventory.csv, which contains:

Date: The date of the sales record

Store ID: Unique identifier for the store

Product ID: Unique identifier for the product

Category: Product category

Region: Geographical region

Units Sold: Number of units sold on the given date

Additional features such as inventory levels, discounts, pricing, weather conditions, and seasonality

Project Steps
Data Loading and Preparation

Load the CSV file into a Pandas DataFrame

Convert the Date column to datetime format

Aggregate sales data by date to get daily total sales

Train-Test Split

The last 30 days of data are used as the test set

The remaining data is used as the training set

Time-based splitting is used to maintain chronological order

Model Training

The Prophet library is used to fit the model on the training data

Future data frames are created for the prediction period

The model forecasts sales for the test period

Model Evaluation

Metrics used:

MAE (Mean Absolute Error)

RMSE (Root Mean Squared Error)

MAPE (Mean Absolute Percentage Error)

Visualization of actual vs. predicted sales

Error distribution plot

Prophet components plot showing trends and seasonality

Results
The project provides sales forecasts for the test period along with accuracy metrics.

Visualization charts display the difference between actual and predicted sales, error distribution, and seasonality trends.

Future Improvements
Integrate region and category-based filtering in predictions

Deploy as an interactive web dashboard using Flask or Dash

Incorporate additional features like weather and promotions into the forecasting model

