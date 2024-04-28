# Cryptocurrency Data Modeling Project

## Table of Contents
1. Introduction
2. Project Overview
3. Executive Summary
4. Project Goals
5. Importance of Machine Learning in Cryptocurrency Trading
6. Approach
7. Data Source Selection and Preparation
8. Model Training Process
9. Sequential Training
10. Aggregation of Predictions
11. Model Complexity
12. Learning Rate Adjustments
13. Regularization Techniques
14. Boosted LSTM Integration
15. Early Stopping
16. Error Monitoring
17. Diverse Initialization
18. Data Results and Visualizations
19. Key Challenges
20. Expected Outcomes
21. Conclusion
22. Next Steps


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


## Project Overview
This project aims to analyze and predict cryptocurrency prices and blockchain activities using machine learning techniques, specifically Long Short-Term Memory (LSTM) networks. The data includes various metrics related to Bitcoin, Ethereum, and Dogecoin, as well as blockchain activity and mining data.
The project overview outlines following factors that were considered when when accessing cryptocurrencies as  potential asset evaluation for the Bitcoin Model.

1. Growing Popularity and Volatility:
   •	Cryptocurrencies, such as Bitcoin, Ethereum, and others, have gained immense popularity in recent years, attracting investors and traders worldwide.
2. Need for Advanced Techniques:
   •	Traditional trading approaches may not suffice in the highly dynamic and unpredictable cryptocurrency markets.
3. Importance of Tailored Strategies:
   •	Cryptocurrency markets exhibit unique characteristics and behaviors compared to traditional financial markets.
   •	Therefore, developing model predictability tailored specifically for cryptocurrencies is essential to account for their distinct dynamics and optimize trading performance.

## Data Selection and Metrics Scope
Coinmetrics is selected for its robustness and reliability in providing comprehensive cryptocurrency market data.
•	The platform offers a wide range of metrics and indicators, allowing for in-depth analysis and modeling of cryptocurrency price movements.
•	Coinmetrics' reputation for data accuracy and integrity makes it a trusted source for building predictive models and making informed trading decisions.
•	Its API and datasets provide convenient access to historical and real-time cryptocurrency data, facilitating seamless integration into the project's workflow.

Coinmetrics provides various data metrics related to cryptocurrencies, including but not limited to:
1. Price Metrics: Such as open, high, low, close prices, and trading volume.
2. Network Metrics: Including hash rate, difficulty, and block size.
3. Transaction Metrics: Such as transaction count, transaction volume, and average transaction value.
4. Mining Metrics: Including miner revenue, miner fees, and block rewards

These metrics provide insights into various aspects of cryptocurrency networks and their ecosystems, enabling analysis, research, and decision-making for traders, investors, researchers, and other stakeholders.

Additional Date Availability CoinMetrics is comprosed of multiple metrics grouped into the following categories:
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

## Slide Show Presentation:

Project 2: BTC_Prediction_Model- Team 3. [Visit Project 2-BTC_Prediction_Model](https://docs.google.com/presentation/d/1GlbIsihWSoSMavqMc0LE-T_36OEocnTH4ASx6DlJhmg/edit?userstoinvite=anderssj%40usc.edu&sharingaction=manageaccess&role=writer#slide=id.g2cf72085fa3_4_33)









