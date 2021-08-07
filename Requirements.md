Requirements
# Introduction
- Stock prices are affected by some obvious factors such as supply and demand, investor sentiment etc and an uncertain noise.
- Investors have always been trying to predict stock prices and make the right choice when buying or selling the stocks.
- StockAstro predicts next day’s closing price for any given stock and also shows the historical stock data (open,close,low,high,volume).
# Research
- Many researchers have published papers in recent years on ‘Stock Price Prediction’ -dealing with improved deep network architectures, sentiment analysis, technical analysis etc. Let’s review some of them while keeping in mind that ‘StockAstro’ is only intended as a fun exercise to practice ‘Software Development Life Cycle’.
1. Authors used dynamic LSTM network that is built using historical stock data and continuously retrained using the newly available data to predict stock prices.

Nguyen, Duc Huu Dat, Loc Phuoc Tran, and Vu Nguyen. ”Predicting stock prices using dynamic lstm models.” International Conference on Applied Informatics Springer, Cham, 2019.

1. Authors implemented various state of the art tree based classifiers such as XGBoost and LightGBM along with deep learning methods such as LSTM and GRU to make a stacked ensemble classifier for stock index prediction.

Jiang, Minqi, et al. ”An improved Stacking framework for stock index prediction by leveraging tree-based ensemble models and deep learning algorithms.” Physica A: Statistical Mechanics and its Applications 541 (2020): 122272.
# Cost and Features
StockAstro is developed using open source tools.
# Features
## Check historical data of any stock
User can choose any stock from anywhere in the world and see it’s historical data.
## Get next day’s closing prediction
For any stock of his/her choosing, user can get prediction for the next day’s closing price.

![](Aspose.Words.b894a8b5-2cdd-4018-b7ca-f3dad8d11aac.001.png)

![](Aspose.Words.b894a8b5-2cdd-4018-b7ca-f3dad8d11aac.002.png)
# 4 W’s and 1 H
## Who
Target audience is stock market investors and machine learning researchers.
## What
A stock predictor driven by machine learning behind the scenes.
## When
It can be used to aid the investor in buy/sell decisions/

## Where
In stock price forecasting. It can be used along with other stock forecasting methods on any platform.
## How
Using FBProphet- a time series analysis tool released by Facebook, it generates a forecast for the next day’s closing price and shows historical data fetched from the yahoo finance API.
# Detail requirements
## High level requirements

|ID|Description|Category|Status|
| :- | :- | :- | :- |
|HR01|User shall be able to search for any stock|Technical|Implemented|
|HR02|User shall be able to read historical data for the selected stock|Technical|Implemented|
|HR04|User shall be able to get next day’s closing prediction|Technical|Implemented|
|HR05|User shall be able to see the confidence interval for the prediction|Technical|Implemented|
|HR06|Stock data should be stored after closing the terminal|Scenario|Future|

## Low level requirements

|ID|Description|HLR ID|Status|
| :- | :- | :- | :- |
|LR01|When searching for any stock, user shall get the stock details to confirm the stock being searched|HR01|Future|
|LR02|In the event of invalid search input, user shall be shown “Invalid Stock” message|HR01|Future|
|LR03|Reading historical data should be possible in two ways: 1) Searching data within given range 2) Searching data for the maximum period|HR02|Future|
|LR04|Along with the next day’s closing price, user shall be shown previous 5 days’ stock data to better aid in buy/sell decision|HR03|Implemented|
|LR04|User shall be given an explanation on confidence interval for the selected stock to better aid the interpretation of the prediction|HR04|Future|
|LR05|User shall be able to save stock data in a file, if a file already exists then overwrite it and if file does not exist then create a new file|HR05|Future|
|LR06|If opening the file fails, then the system should download the same and should not end the program execution|HR01, HR02, HR06|Future|


