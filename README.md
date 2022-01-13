# LSTM-BTC-Predictor
### Comparison of two models using LSTM. The first one is based on a sentiment analysis and the second on the closing prices

The purpose here is to make a model with identical parameters and determine which one fits best to predict BTC prices.

The LSTM model that seems to fit the best has the following paramaters:<br>
 > window = 2 <br>
    nodes = 6 <br>
    layers = 3 <br>
    dropout = 0.2 <br>
    optimizer = adam <br>
    loss = mean_squared_error <br>
>   validation_split = 0.2

The remaining difference between those two models is the input. The closing price and the Crypto Fear and Greed Index (FNG).

* *Which model has a lower loss?* <br>
The closing price model has a significantly better performance with a loss of 0.0166

* *Which model tracks the actual values better over time?* <br>
The closing price model tracks the values with certain accuracy. This is not the case of the FNG model. This second models looks like a flat line, with some important up and down movement when the real price is having a slope change. We could consider that a major change in FNG predicts an important change for the real price.


* *Which window size works best for the model?* <br>
A window size of 10 had a flattening effect on the test, I found out that a smaller window tended to show a better results. A 2 day window is the optimal result in this case