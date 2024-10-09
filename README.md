# MachineLearning CryptoCurrency Predictor
This project predict sshort-term cryptocurrency price movements using minute-by-minute historical data. We developed machine learning models to classify whether the price of a cryptocurrency asset will go up (1) or stay the same/move down (0) in the next minute.
## Dataset
timestamp: Unix timestamp for the minute covered by the row.
open, high, low, close: OHLC prices of the asset.
volume: Number of cryptocurrency units traded.
quote_asset_volume: Total value of traded shares.
number_of_trades: Number of trades in the given minute.
taker_buy_base_volume: Volume bought by takers.
taker_buy_quote_volume: Value of volume bought by takers.
target: Binary classification target (1 = price goes up, 0 = price stays the same or goes down).
## Engineered Features
Moving Averages: 5-minute and 15-minute moving averages of the close price to capture short-term trends.
Momentum: Difference between the current and previous minute's closing price.
Volatility: Rolling standard deviation of the close price over a 5-minute window.
## Data Model
### Logistic Regression
![image](https://github.com/user-attachments/assets/3d526fc1-5782-47a5-bd97-930c65892298)

### Random Forest
![image](https://github.com/user-attachments/assets/c7cc7e5a-e3e5-4502-b073-515a2e725837)

### XGBoost
![image](https://github.com/user-attachments/assets/e228a3b6-bea0-47b7-8f04-7eecc6ca6848)

![image](https://github.com/user-attachments/assets/d2c9d19d-5f3f-4405-be19-280d14432783)

### SHAP
We used SHAP (SHapley Additive exPlanations) to explain the model’s predictions by analyzing how much each feature contributed to the decision.

Key Features:
Close Price: Strong influence on predictions.
Momentum: High momentum values indicate likely upward price movement.
Volatility: High volatility impacts both upward and downward predictions.
![image](https://github.com/user-attachments/assets/042ba5f4-f603-433c-872c-3199ef4b934f)


![image](https://github.com/user-attachments/assets/d0649169-5281-42e9-b445-9e7d81f2788e)

### Conclusion 
This project successfully built a machine learning pipeline to predict short-term cryptocurrency price movements. We experimented with various features and models, concluding that XGBoost performed best based on F1 scores. Using SHAP analysis, we identified the most important features driving model predictions.
