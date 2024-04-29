# Cryptocurrency Data Modeling Project

## Table of Contents
1. Introduction
2. Project Overview (#overview)
4. Executive Summary
5. Project Goals
6. Importance of Machine Learning in Cryptocurrency Trading
7. Approach
8. Data Source Selection and Preparation(#data-description)
9. Model Training Process
10. Sequential Training
11. Aggregation of Predictions
12. Model Complexity
13. Learning Rate Adjustments
14. Regularization Techniques
15. Boosted LSTM Integration
16. Early Stopping
17. Error Monitoring
18. Diverse Initialization
19. Data Results and Visualizations
20. Key Challenges
21. Expected Outcomes
22. Conclusion
23. Next Steps


1. [Overview]
2. [Data Description]
3. [Steps](#steps)
   - [Step 1: Data Collection](#step-1-data-collection)
   - [Step 2: Data Preprocessing](#step-2-data-preprocessing)
   - [Step 3: Model Building and Evaluation](#step-3-model-building-and-evaluation)
   - [Step 4: Implementation of Boosted LSTM](#step-4-implementation-of-boosted-lstm)
4. [Requirements](#requirements)
5. [Usage](#usage)
6. [Acknowledgments](#acknowledgments)
7. [References](#references)

## Executive Summary:
Project Objective:

•	The primary objective of this project is to develop a Bitcoin Prediction Model specifically designed for cryptocurrency markets.
•	By leveraging advanced machine learning techniques, our goal is to create a robust framework capable of making informed trading decisions in the rapidly evolving     cryptocurrency landscape.

## Project Overview:
This project aims to analyze and predict cryptocurrency prices and blockchain activities using machine learning techniques, specifically Long Short-Term Memory (LSTM) networks. The data includes various metrics related to Bitcoin, Ethereum, and Dogecoin, as well as blockchain activity and mining data.
The project overview outlines following factors that were considered when when accessing cryptocurrencies as  potential asset evaluation for the Bitcoin Model.

1. Growing Popularity and Volatility:
   •	Cryptocurrencies, such as Bitcoin, Ethereum, and others, have gained immense popularity in recent years, attracting investors and traders worldwide.
2. Need for Advanced Techniques:
   •	Traditional trading approaches may not suffice in the highly dynamic and unpredictable cryptocurrency markets.
3. Importance of Tailored Strategies:
   •	Cryptocurrency markets exhibit unique characteristics and behaviors compared to traditional financial markets.
   •	Therefore, developing model predictability tailored specifically for cryptocurrencies is essential to account for their distinct dynamics and optimize trading performance.

## Data Selection and Metrics Scope:
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

## Project Goals:
1. Developing Machine Learning Models:
   - Our primary goal is to develop machine learning models capable of accurately predicting cryptocurrency price movements.
   - Leveraging historical price data and relevant market indicators, we aim to train sophisticated models, such as Long Short-Term Memory (LSTM) networks, to forecast future price trends with high precision.

2. Implementing Ensemble Methods:
   - In addition to individual machine learning models, we intend to implement ensemble methods to further enhance prediction accuracy and robustness.
   - Ensemble methods combine the predictions of multiple models to produce a collective forecast that often outperforms any single model. By integrating diverse          perspectives and approaches, ensemble methods can effectively capture the complexity of cryptocurrency markets.

3. Optimizing Trading Decisions:
   - Beyond prediction, our project seeks to optimize trading decisions in the cryptocurrency market.
   - By integrating machine learning predictions with sophisticated trading algorithms, we aim to maximize returns and mitigate risks associated with cryptocurrency trading.
   - Through systematic analysis of market signals and adaptive decision-making, our goal is to develop a trading strategy that capitalizes on opportunities while    
     minimizing potential losses.

4. Maximizing Returns and Mitigating Risks:
   - Ultimately, our overarching goal is to maximize returns for investors while simultaneously mitigating risks inherent in the cryptocurrency market.
   - By leveraging advanced machine learning techniques and ensemble methods, we aspire to achieve a balance between profitability and risk management, thereby 
     delivering value to our stakeholders.


## Importance of Machine Learning in Cryptocurrency Trading:
The project lies at the intersection of fintech and machine learning, leveraging advanced algorithms to analyze cryptocurrency data and make informed trading decisions.
   - Machine learning enables us to analyze vast amounts of cryptocurrency data and extract meaningful insights for making informed trading decisions.
   - LSTM models, in particular, have shown promise in capturing complex patterns and trends in cryptocurrency price data, leading to improved prediction accuracy    
     and trading performance.


## Approach:
   1. Data Collection: Gather cryptocurrency data from reliable sources such as Coinmetrics (exchanges, APIs, and historical databases) to capture a comprehensive    
      dataset of price movements.
   2. Data Preprocessing: Prepare the data for analysis by cleaning-Remove errors or inconsistencies, normalizing-Standardize data ranges to avoid model bias, and
      feature Engineering-Develop new variables from existing data to enhance model predictions.
   3. Model development: Train LSTM models on the prepared dataset and implement ensemble methods to aggregate predictions and optimize trading decisions.
   4. Evaluation: Evaluate model performance using relevant metrics such as accuracy, mean squared error, and profitability to ensure the effectiveness of the    
      trading strategy.
      
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



## Model Training Process:
     - We trained an initial LSTM model on the cryptocurrency dataset to establish a baseline for prediction.
     - The model was trained using historical cryptocurrency price data, market indicators, and blockchain metrics to learn patterns and trends in the data.
     - Training parameters such as batch size, epochs, and optimizer settings were tuned to optimize model performance.

### Wavelet Transforms
   -Denoising and Signal Extraction of temporal data, excellent in analyzing non-stationary data  
   -Passes the signal through different filters to analyze frequency components at different scales
   
Wavelet transforms can be utilized as a preprocessing step to enhance the quality of the input data before feeding it into the model.
   1. **Denoising and Signal Extraction:** Before training the model, temporal data, such as cryptocurrency price series, often contains noise or irrelevant       
   fluctuations. Applying wavelet transforms helps denoise the data by separating the signal from the noise. This ensures that the model focuses on learning 
   meaningful patterns rather than being influenced by irrelevant fluctuations.

   2. **Analysis of Non-Stationary Data:** Cryptocurrency price data is inherently non-stationary, meaning its statistical properties change over time. Wavelet 
   transforms excel in analyzing such data by decomposing it into different frequency components at varying scales. This decomposition enables the model to capture 
   complex temporal patterns and variations present in the cryptocurrency market.

By integrating wavelet transforms into the model training process, we can preprocess the data effectively, enhancing the model's ability to learn and extract relevant features for predicting cryptocurrency price movements.


### Feature Engineering
Lagged values, Rolling Windows, Standard deviation
In the model training process, feature engineering plays a crucial role in preparing the input data to be fed into the machine learning model. Here's how each of the mentioned feature engineering techniques—lagged values, rolling windows, and standard deviation—is tied to the model training process:

1. **Lagged Values:**
   - **Implementation:** Lagged values involve including past observations of relevant variables as features in the dataset. This can be implemented by shifting the time series data by a certain number of time steps to create lagged features.
   - **Training:** During model training, the dataset containing lagged values is used to train the machine learning model. The model learns from the historical patterns and relationships between lagged values and target variables to make predictions.

2. **Rolling Windows:**
   - **Implementation:** Rolling windows involve calculating summary statistics (e.g., mean, median) over a fixed window of past observations. This can be implemented using functions like `rolling()` in pandas or custom functions to calculate statistics over specific time windows.
   - **Training:** The dataset with rolling window features is used to train the machine learning model. These features provide temporal context and capture trends over time, allowing the model to learn from the evolving nature of the data.

3. **Standard Deviation:**
   - **Implementation:** Standard deviation measures the dispersion or variability of a dataset. It can be calculated over a rolling window or for lagged values to capture volatility in the data.
   - **Training:** Including standard deviation as a feature provides information about the variability of the underlying data. During model training, the model learns from these features to understand the level of volatility in the dataset and its impact on the target variable.

By incorporating lagged values, rolling windows, and standard deviation as features in the training dataset, the machine learning model can learn from the temporal patterns and variability present in the data, ultimately leading to more robust and accurate predictions.

### Sequence Creation
Sequence creation is a fundamental step in preparing time series data for training sequence models. By organizing the data into sequences and encoding them appropriately, we enable the model to learn from the temporal dynamics of the data and make accurate predictions over time.

### Model Architecture
Model architecture choices, including activation functions, the number of layers, and hidden units, play a critical role in shaping the behavior of the model during training. These decisions influence how the model learns from the data, the complexity of representations it can capture, and its overall performance on the task at hand.

### Hyperparameter Tuning
Boosted LSTM Integration
Allows subsequent LSTM models to target remaining patterns or nuances insufficiently captured by earlier models
Provides a more accurate prediction model than non-boosted integrations.


## Sequential Training :
   - After training the initial LSTM model, we implemented sequential training to improve prediction accuracy.
   - Additional LSTM models were trained on residuals or errors between predicted and actual values to capture missed patterns.
   - Each subsequent model focused on learning from the residuals left by its predecessors, leading to iterative improvement in prediction performance.


## Aggregration Predictions :
   - This approach is commonly used in machine learning and data science to enhance transparency and understanding of such predictive models.
     There are several ways to aggregate predictions in machine learning.
   - This would be the process of combining explainations from multiple prediction models or sources into a cohesive understanding.
   - Predictions from multiple LSTM models were aggregated using weighted averaging.
   - The weights for each model were determined based on its performance on a validation dataset, with higher-performing models given more weight in the final    
     prediction.











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









