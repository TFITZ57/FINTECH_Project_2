# Cryptocurrency Data Modeling Project

## Table of Contents
1. [Overview](#overview)
2. [Data Description](#data-description)
3. [Steps](#steps)
   - [Step 1: Data Collection](#step-1-data-collection)
   - [Step 2: Data Preprocessing](#step-2-data-preprocessing)
   - [Step 3: Model Building and Evaluation](#step-3-model-building-and-evaluation)
   - [Step 4: Implementation of Boosted LSTM](#step-4-implementation-of-boosted-lstm)
4. [Requirements](#requirements)
5. [Usage](#usage)
6. [Acknowledgments](#acknowledgments)
7. [References](#references)


## Overview
This project aims to analyze and predict cryptocurrency prices and blockchain activities using machine learning techniques, specifically Long Short-Term Memory (LSTM) networks. The data includes various metrics related to Bitcoin, Ethereum, and Dogecoin, as well as blockchain activity and mining data.

## Data Description
The dataset from CoinMetrics is comprosed of multiple metrics grouped into the following categories:
- **Basic Price Information**: Prices of BTC, ETH, and DOGE in USD.
- **Blockchain Activity Metrics**: Active addresses, transaction count, value, block difficulty, and total fees in USD.
- **Mining and Revenue Metrics**: Mining revenue, hash rate, hash price, and Bitcoin held by miners.
- **Market and Economic Indicators**: SOPR, MVRV Ratio, and Rev. Puell Multiple.
- **Volatility and Network Flows**: Realized volatility over different periods and netflows from/to exchanges.
- **Lagged Price Data**: Historical price data for time-series analysis.

## Steps

### Step 1: Data Collection
- Data is sourced from various reliable crypto analytics platforms.

### Step 2: Data Preprocessing
- Includes cleaning, handling missing values, outlier detection, and feature engineering such as timestamp decomposition and rolling window statistics.

### Step 3: Model Building and Evaluation
- Using LSTM networks to capture temporal dependencies within the data.
- Models are evaluated based on their prediction accuracy and ability to generalize using time series cross-validation.

### Step 4: Implementation of Boosted LSTM
- Boosting technique is applied to LSTM to enhance model performance by focusing on the residuals of previous models.

## Requirements
- Python 3.x
- Libraries: pandas, numpy, tensorflow, keras, matplotlib, seaborn, sklearn, pywt (for wavelet transforms)

## Installation and Usage

To run this project, you will need to have the following dependencies installed:

- Python (version 3.6 or later)
- Jupyter Notebook or VSCode
- Pandas
- Scikit-Learn
- TensorFlow
- Seaborn (optional, for data visualization)
- hvPlot (optional, for interactive visualizations)

1. Clone the repository to your local machine.
2. Navigate to the project directory.
3. Install the required dependencies in your terminal or command prompt.
5. Open the relevant Jupyter Notebook file(s) and run the cells to train the model, make predictions, and visualize the results.

## Examples and Results
screenshots showcasing the application and visualizations:


## Acknowledgments
* CoinMetrics API for providing access to their comprehensive crypto data.
* Community contributions and suggestions that helped shape the analysis.

## References

- CoinMetrics: Comprehensive data and insights for cryptocurrencies. [Visit CoinMetrics](https://coinmetrics.io/)
- IntoTheBlock: Detailed blockchain data and analytics for Bitcoin and other cryptocurrencies. [Access IntoTheBlock](https://app.intotheblock.com/coin/BTC)
- Bitcoin Visuals: Graphs and statistics that provide insights into the Bitcoin network. [See Bitcoin Visuals](https://bitcoinvisuals.com/)
- DeFi Llama API Documentation: Access comprehensive DeFi data through APIs. [Read DeFi Llama Docs](https://defillama.com/docs/api)
- Federal Reserve Economic Data (FRED) API: Economic data from the Federal Reserve Bank of St. Louis. [Explore FRED API](https://fred.stlouisfed.org/docs/api/fred/)
- Stock to Flow Model: Understand the relationship between production and current stock available, used for predicting Bitcoin prices. [Learn about Stock to Flow](https://stocktoflow.com/)
- Twitter API Reference: Official API documentation for accessing Twitter data programmatically. [Twitter API Docs](https://developer.twitter.com/en/docs/api-reference-index)


