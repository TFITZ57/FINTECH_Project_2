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


## Model Complexity :
   - We carefully considered the complexity of each LSTM model in the ensemble to balance model performance and overfitting.
   - Model complexity was adjusted by varying the number of LSTM units, layers, and other architectural parameters to achieve optimal performance.


## Regularization Techniques :
Regularization techniques are essential components of the Bitcoin Prediction Model, designed to prevent overfitting and improve the model's generalization performance. Here's how regularization techniques are applied in the context of the Bitcoin Prediction Model, as demonstrated in the previous code and slide show:

1. **Dropout:**
   - Dropout is a widely used regularization technique that involves randomly deactivating a fraction of neurons during training, effectively introducing noise and 
     preventing co-adaptation of neurons.
   - In the Bitcoin Prediction Model, dropout layers can be incorporated into the LSTM architecture to randomly drop units (neurons) along with their connections 
     during training.
   - By randomly dropping units, dropout helps prevent over-reliance on specific features or neurons, encouraging the model to learn more robust and generalizable 
     representations.

2. **L1/L2 Regularization:**
   - L1 and L2 regularization impose penalties on the model's weights to discourage overly complex solutions and prevent overfitting.
   - In the context of the Bitcoin Prediction Model, L1 and L2 regularization terms can be added to the loss function during training, penalizing large weights.
   - L1 regularization (Lasso) adds the absolute value of the weights to the loss function, encouraging sparsity by driving some weights to zero.
   - L2 regularization (Ridge) adds the squared magnitude of the weights to the loss function, penalizing large weights without driving them to zero.
   - By adding regularization terms to the loss function, L1/L2 regularization encourages the model to learn simpler and more generalizable patterns from the data, 
     reducing the risk of overfitting.

3. **Recurrent Dropout:**
   - Recurrent Dropout is a variant of dropout specifically designed for recurrent neural networks (RNNs) like LSTM.
   - In the Bitcoin Prediction Model, recurrent dropout can be applied to the LSTM layers to randomly mask inputs or states during training.
   - By randomly masking inputs or states, recurrent dropout prevents LSTM cells from memorizing sequences too perfectly, promoting better generalization to unseen 
     data.

4. **Implementation:**
   - Regularization techniques such as dropout, L1/L2 regularization, and recurrent dropout can be implemented using TensorFlow's built-in layers or custom 
     regularizers.
   - These regularization techniques are typically configured during the construction of the LSTM model, allowing for fine-tuning of regularization strength and 
     application to specific layers.
   - By incorporating regularization techniques into the Bitcoin Prediction Model, the model becomes more resilient to overfitting and better equipped to make 
     accurate predictions on unseen cryptocurrency price data.

In summary, regularization techniques play a crucial role in enhancing the Bitcoin Prediction Model's performance by preventing overfitting and improving generalization. By incorporating dropout, L1/L2 regularization, and recurrent dropout, the model becomes more robust and reliable for predicting cryptocurrency price movements in dynamic market conditions.


## Expected Outcomes: 
In the absence of concrete data results, it's still possible to outline the expected outcomes of the project based on the methodology, model architecture, and training process. Here's how you can describe the expected outcomes despite the lack of data results:

1. **Improved Prediction Accuracy:**
   - The primary objective of developing the Bitcoin Prediction Model was to improve prediction accuracy for cryptocurrency price movements.
   - Based on the chosen methodology, including the use of LSTM models, ensemble methods, and regularization techniques, the expected outcome would have been a more 
     accurate prediction of cryptocurrency prices compared to baseline models or traditional methods.

2. **Enhanced Trading Strategy Performance:**
   - With improved prediction accuracy, the expected outcome would have been an enhancement in the performance of the algorithmic trading strategy.
   - By leveraging machine learning techniques and ensemble methods, the Bitcoin Prediction Model aimed to optimize trading decisions and maximize returns while 
     mitigating risks in the cryptocurrency market.

3. **Contribution to Algorithmic Trading Research:**
   - Beyond specific prediction results, the project aimed to contribute to the growing field of algorithmic trading research, particularly in the context of 
     cryptocurrency markets.
   - The methodology, model architecture, and training process employed in the project could provide valuable insights and serve as a foundation for future research 
     and development i gorithmic trading strategies for cryptocurrencies.

4. **Validation of Methodological Approach:**
   - Despite the absence of data results, the project aimed to validate the effectiveness of the chosen methodological approach.
   - By carefully selecting machine learning techniques, optimizing model architecture, and addressing challenges in data preprocessing and model training, the 
     expected outcome was to demonstrate the viability and robustness of the approach for predicting cryptocurrency prices.

5. **Insights into Model Performance and Generalization:**
   - Although quantitative results may not be available, the project aimed to provide qualitative insights into model performance and generalization.
   - Through thorough analysis of the training process, evaluation metrics, and potential areas of improvement, the expected outcome was to gain valuable insights into the strengths and limitations of the Bitcoin Prediction Model.

6. **Demonstration of Methodological Rigor:**
   - Despite the absence of data results, the project aimed to demonstrate methodological rigor and adherence to best practices in machine learning and algorithmic 
     trading research.
   - By documenting the approach, methodology, and decision-making process, the expected outcome was to showcase a systematic and well-structured approach to solving 
     complex problems in cryptocurrency trading.

By outlining these expected outcomes, even in the absence of data results, you can provide a clear understanding of the project's objectives, motivations, and anticipated contributions to the field of algorithmic trading for cryptocurrencies.


## Data Results and Mitigating Facotrs :
In the absence of data results to showcase for the project, it's essential to provide extensive detail on various aspects of the project, including the methodology, model architecture, training process, challenges faced, and potential insights gained. 

1. **Methodology Overview:**
   - Begin by providing a comprehensive overview of the project's methodology, including the steps involved in developing the Bitcoin Prediction Model.
   - Explain the rationale behind selecting specific machine learning techniques, such as LSTM models, ensemble methods, and regularization techniques, for predicting cryptocurrency price movements.
   - Describe the approach taken for data collection, preprocessing, and feature engineering to prepare the cryptocurrency price data for model training.

2. **Model Architecture and Training Process:**
   - Provide detailed insights into the architecture of the Bitcoin Prediction Model, including the number of LSTM layers, hidden units, activation functions, and regularization techniques used.
   - Explain the sequential training process, where additional LSTM models are trained on residuals to capture missed patterns in the data.
   - Describe how model complexity was carefully chosen to balance performance and generalization, highlighting the trade-offs involved in selecting the optimal model architecture.

3. **Challenges Faced:**
   - Discuss the challenges encountered during the project, such as data availability, model convergence, hyperparameter tuning, and computational resources.
   - Explain how these challenges were addressed or mitigated throughout the project, demonstrating adaptability and problem-solving skills.

4. **Insights Gained:**
   - Despite the absence of concrete data results, highlight any qualitative insights or observations gained during the model development process.
   - Discuss the potential implications of the project findings for cryptocurrency trading and algorithmic trading strategies, even if quantitative results are not available.

5. **Future Directions and Next Steps:**
   - Conclude the presentation by outlining potential future directions and next steps for the project.
   - Discuss areas for further research, such as exploring alternative machine learning techniques, incorporating additional data sources, or refining the model architecture.
   - Emphasize the iterative nature of the project and the continuous pursuit of improvement and innovation in algorithmic trading strategies for cryptocurrency markets.

## Conclusions:
Despite the absence of concrete data results, the culmination of this project offers valuable insights and reflections on the journey of developing a Bitcoin Prediction Model tailored for cryptocurrency markets. Here's an extensive conclusion based on the lack of results:

1. **Reflection on the Project Objective:**
   - The primary objective of this project was to develop a robust algorithmic trading strategy specifically designed for cryptocurrency markets. While the intended goal was to achieve improved prediction accuracy and enhance trading strategy performance, the absence of concrete data results necessitates a deeper reflection on the methodology and approach adopted.

2. **Methodological Insights and Challenges:**
   - Throughout the project, significant emphasis was placed on methodological rigor and the application of advanced machine learning techniques, such as LSTM models, ensemble methods, and regularization techniques. Despite meticulous planning and execution, the absence of data results underscores the inherent challenges and complexities involved in predicting cryptocurrency prices accurately.
   - Challenges such as high market volatility, limited availability of historical data, and the need for real-time analysis pose significant hurdles in developing reliable prediction models for cryptocurrency trading. The absence of tangible results serves as a reminder of the unpredictable nature of cryptocurrency markets and the inherent risks associated with algorithmic trading in this domain.

3. **Lessons Learned and Future Directions:**
   - While the project did not yield concrete data results, it provides valuable lessons and insights for future research and development in algorithmic trading for cryptocurrencies. The journey of data collection, preprocessing, model training, and evaluation has offered valuable experiential learning, highlighting the importance of flexibility, adaptability, and continuous improvement in algorithmic trading strategies.
   - Moving forward, future research efforts could focus on addressing the challenges identified during this project, such as refining data preprocessing techniques, exploring alternative machine learning architectures, and incorporating additional data sources to improve prediction accuracy and robustness.
   - Additionally, the project underscores the importance of interdisciplinary collaboration between domain experts, data scientists, and industry practitioners in tackling complex problems in cryptocurrency trading. By leveraging a diverse range of expertise and perspectives, future endeavors in algorithmic trading research can strive to overcome challenges and achieve meaningful advancements in the field.

4. **Conclusion and Outlook:**
   - In conclusion, while the absence of data results may seem like a setback, it serves as a catalyst for reflection, learning, and growth. The journey of developing a Bitcoin Prediction Model has been a valuable experience, offering insights into the intricacies of algorithmic trading in cryptocurrency markets.
   - As we navigate the dynamic landscape of cryptocurrency trading, the lessons learned from this project will undoubtedly inform future endeavors, shaping the trajectory of algorithmic trading research and innovation. While the road ahead may be challenging, it is also ripe with opportunities for discovery, collaboration, and advancement in the fascinating intersection of finance, technology, and data science.

By embracing the lessons learned from this project and maintaining a spirit of curiosity and resilience, we can continue to push the boundaries of knowledge and make meaningful contributions to the ever-evolving field of algorithmic trading for cryptocurrencies.


## Next Steps:
In light of the absence of data results, the project's next steps would focus on several key areas aimed at addressing the challenges encountered and further refining the algorithmic trading strategy for cryptocurrency markets. Here's an extensive detail on the next steps:

1. **Refinement of Data Collection and Preprocessing Techniques:**
   - Given the challenges associated with data availability and quality, the next step would involve refining data collection and preprocessing techniques. This could include exploring alternative data sources, such as blockchain data or sentiment analysis from social media, to supplement existing datasets. Additionally, efforts would be directed towards improving data cleaning, normalization, and feature engineering processes to enhance the quality and relevance of input data for model training.

2. **Exploration of Alternative Machine Learning Architectures:**
   - In light of the limitations encountered with LSTM models and ensemble methods, the project would explore alternative machine learning architectures tailored specifically for cryptocurrency price prediction. This could involve investigating deep learning architectures like convolutional neural networks (CNNs) or transformer models, which may offer improved capabilities in capturing complex patterns and trends in cryptocurrency data.

3. **Integration of External Factors and Indicators:**
   - Recognizing the multifaceted nature of cryptocurrency markets, future efforts would focus on integrating external factors and indicators into the prediction model. This could include incorporating macroeconomic indicators, regulatory developments, and market sentiment analysis to augment the predictive capabilities of the algorithmic trading strategy. By considering a broader range of factors, the model can better adapt to changing market conditions and improve prediction accuracy.

4. **Implementation of Advanced Trading Strategies:**
   - Building upon the foundation of the algorithmic trading strategy, the next steps would involve implementing advanced trading strategies to optimize decision-making and risk management. This could include the development of dynamic portfolio allocation techniques, algorithmic execution strategies, and risk-adjusted performance metrics to enhance overall trading performance and profitability.

5. **Evaluation and Validation Framework Enhancement:**
   - To ensure the robustness and reliability of the algorithmic trading strategy, future efforts would focus on enhancing the evaluation and validation framework. This could involve implementing more rigorous backtesting procedures, conducting out-of-sample testing on unseen data, and incorporating statistical techniques for performance analysis and risk assessment. By rigorously evaluating the model's performance under diverse market conditions, we can gain confidence in its effectiveness and generalizability.

6. **Continuous Learning and Adaptation:**
   - Finally, the project's next steps would emphasize a culture of continuous learning and adaptation. This includes staying updated on the latest research advancements in algorithmic trading, cryptocurrency markets, and machine learning techniques. Additionally, maintaining an open dialogue with domain experts, industry practitioners, and academic researchers can provide valuable insights and perspectives to inform future iterations of the algorithmic trading strategy.

By focusing on these next steps, the project aims to overcome the challenges posed by the absence of data results and further refine the algorithmic trading strategy for cryptocurrency markets. Through iterative experimentation, innovation, and collaboration, we can continue to push the boundaries of knowledge and drive meaningful advancements in algorithmic trading research and practice.


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









