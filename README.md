# Gold-Price-Forecasting

This repository contains code for predicting gold prices using historical data and a Random Forest Regressor model. The model is trained on key features such as Silver (SLV), S&P 500 (SPX), and year-based features, and predicts the closing gold price (`GLD`).

## Dataset

The dataset used in this project is `gold_price_data.csv`, which contains historical gold price data along with features like:

- **Date**: The date of the data point.
- **GLD**: The closing price of gold.
- **SLV**: The price of silver.
- **SPX**: The S&P 500 index value.

## Features Engineered

The following features are engineered from the `Date` column:

- **Year**: The year extracted from the Date.
- **Month**: The month extracted from the Date.
- **Day**: The day extracted from the Date.
- **DayOfWeek**: The day of the week, where 0 = Monday and 6 = Sunday.
- **Quarter**: The quarter of the year.

## Steps Involved

1. **Data Preprocessing**:
    - Loading the dataset and checking for missing values.
    - Converting the `Date` column to a datetime object and extracting new time-based features.
    - Dropping the original `Date` column.
    - Visualizing the correlation between features using a heatmap.

2. **Feature Selection**:
    - Selecting relevant features such as `SLV`, `Year`, and `SPX` for the prediction model.
    - Creating a new DataFrame with the target variable `GLD` and the relevant features.

3. **Model Training**:
    - Splitting the data into training and testing sets (80% training, 20% testing).
    - Training a Random Forest Regressor model on the training data.

4. **Model Evaluation**:
    - Evaluating the model's performance using the R² score (coefficient of determination).
    - Comparing the actual vs predicted gold prices using a line plot.

## Results

The model provides an R² score to evaluate how well the predictions match the actual gold prices. The predictions are also visualized using a line plot, which compares actual and predicted gold prices.

