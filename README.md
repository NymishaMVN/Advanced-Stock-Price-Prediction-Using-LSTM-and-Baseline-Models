1.Business Problem
With the stock market being so volatile, it is very important for investors, 
analysts, and financial institutions to make wise decisions. Standard 
statistical models usually cannot catch the irregularities and relationships 
present in financial time-series. Through the usage of Long Short-Term 
Memory (LSTM) and Gated Recurrent Unit (GRU) networks, the project 
intends to foresee the prices of stocks from certain publicly traded 
companies.
By creating, checking, and comparing these models, the aim is to give more 
accurate forecasts for the near future, helping both in investments and in 
handling risks. Also, to confirm the robustness and how well the model 
works in general, it is assessed using both a single data split and crossvalidation.

2.Approach
Data Collection:
We used the yfinance package to get historical stock prices for five 
companies:
- Apple (AAPL)
- Boeing (BA)
- General Dynamics (GD)
- Huntington Ingalls Industries (HII)
- Lockheed Martin (LMT)
  
Data Preprocessing
Normalization: We have used Applied MinMaxScaler to make sure all 
prices are scaled between 0 and 1.
Sequence Preparation: Transformed the time-series into forms that 
supervised learning algorithms could use by sliding a window of 100 steps 
down the data series.

Modeling Techniques
LSTM Neural Network: Identifies long-term situations and patterns where 
each event follows another.
GRU Neural Network: A quick and simple alternative to LSTM that works 
as well.

Evaluation Strategy 
1. 70/20/10 Split:
 - 70% Training
 - 20% Validation
 - 10% Testing
   
2. Cross-Validation:
 We used the time series split strategy with 5 folding to check the 
performance of the model at different time points.

3. Performance Metrics:
 - Root Mean Squared Error (RMSE)
 - R-Squared (R² Score)
   
4. Future Forecasting:
 - Created 10-day forecasts using two models, using the latest information.
 - 
3.Key Findings
Model Performance:
- Both LSTM and GRU achieved good results for each of the tickers.
- For several cases, GRU proved to be both fast in training and capable of 
generalizing well.
Both models proved stable and consistent after being tested with cross validation.

Forecasting Results:
We can forecast the next 10 days of trading for every ticker selected.
- The generated visualizations and values correctly showed how the models 
could be used in the current market.

Business Implications:
- The models support and make possible fast-paced investing decisions.
- They can be built into decision-support systems used by analysts and 
investors.
Using cross-validation gives additional assurance that the model can reliably 
be put into practice.

4.Conclusion and Next Steps
This work reveals that LSTM and GRU models perform well when trying to 
predict stock prices from past data. Although no model is 100% accurate in 
finance, these models help provide useful, statistically backed predictions 
over the short run.
