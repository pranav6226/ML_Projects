
# README

## Executive Summary
This project leverages machine learning to estimate the last price valuation in options trading, focusing on SPX options data from 2023. Accurate predictions of the closing price of options enable traders to optimize their exit strategies, potentially compounding gains under favorable conditions.

## Business Problem
In the complex world of options trading, accurately predicting the final price of an option at expiration can significantly improve trading outcomes. This project addresses this challenge by developing a machine learning model designed to predict the last price of SPX options, helping traders make informed decisions on when to exit their positions to maximize profitability.

## Methodology

### Data Collection and Exploration (EDA)
1. **Data Sourcing:** The data for this project was sourced from "optionsdx.com", specifically focusing on SPX options chain data for the entire year of 2023. The data was structured into four quarterly folders, each containing files for three months.
2. **Initial Data Exploration:**
   - The date range of the data was verified to ensure completeness.
   - Null values were identified and handled through various methods, including merging with external datasets and forward-filling missing data.

### Data Preprocessing
1. **Data Merging:**
   - **Risk-Free Rate Data:** The options data was merged with data from the Federal Reserve Economic Data (FRED), which provided the risk-free rate. Missing values in this data were imputed using a feed-forward technique.
   - **Spot Price Data:** Spot price data was sourced from Yahoo Finance and merged with the options dataset.
2. **Handling Null Values:**
   - After merging, null values were checked and rows containing nulls were dropped to ensure data integrity.
3. **Data Cleaning:**
   - Column names were cleaned by removing square brackets and unnecessary white spaces to ensure consistency in the dataset.

### Feature Engineering
1. **Normalization and Scaling:**
   - The data was normalized and scaled to prepare it for model training. This step ensured that all features contributed equally to the model's learning process.
2. **Additional Feature Creation:**
   - Additional columns were created to enhance the dataset, such as calculating implied volatility, moneyness, and other key financial metrics relevant to options trading.

### Model Development
1. **Model Selection:**
   - Various machine learning models were considered, with a focus on predicting the last price of the options.
2. **Training and Evaluation:**
   - The selected model was trained on the processed dataset, and its performance was evaluated using relevant metrics to ensure accuracy and reliability.

## Skills
- Data Collection and Preprocessing
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Machine Learning Model Development
- Predictive Analytics
- Python Programming
- Financial Data Analysis

## Results
The project successfully developed a machine learning model capable of predicting the last price of SPX options with a focus on short-term expiration dates. The model's predictions provide valuable insights for traders looking to optimize their exit strategies and compound gains in options trading.

## Next Steps
- **Model Refinement:** Further optimization of the machine learning model to enhance prediction accuracy.
- **Expand Data Scope:** Incorporate additional data sources and expand the analysis to include other types of options and expiration dates.
- **Deployment:** Develop a user-friendly interface or dashboard to allow traders to utilize the model's predictions in real-time.
- **Backtesting:** Implement a backtesting framework to validate the model's performance in historical trading scenarios.
