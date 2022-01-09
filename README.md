# ML-Algorithmic-Trading


![ml_image](Resources/ML_image.png)


Optimizing Trading Signals with Machine Learning

---

This jupyter notebook file includes:

- Algorithmic trading strategy that uses machine learning to automate trade decisions.
- Adjusted input parameters to optimize the trading algorithim.
- A Summary of 2 distinct machine learning models and a comparison of performance of tuned models to baseline model.

## Technologies

This project uses Python 3.7 with the following packages and modules:

-Pandas

-Numpy

-Pathlib

-Matplotlib

-Sklearn


## Installation Guide

This analysis was done with Pandas in Jupyter Lab. If the User wants to interact with the Machine Learning Model, first install the following:
  To get started using this application please go to [Python Download](https://www.python.org/downloads/) and select the version for your operating system. Then install the following libraries and packages.

``` sudo apt install python3-pip ```. This will install the pip that will make it easier to install the libraries.

``` pip install pandas ```

``` pip install numpy ```

``` pip install -U scikit-learn ```

``` python -m pip install -U pip ```

``` python -m pip install -U matplotlib ```


## Usage

The file of interest is labeled ``` machine_learning_trading_bot.ipynb ```


## Contributors

Stephen Thomas

[Trilogy Education Services](https://www.trilogyed.com/)

[UC Berkeley Extension ](https://extension.berkeley.edu/)



## License 

MIT
---

# Summary Evaluation Report

This report will explain and compare the different iterations of machine learning models that were built, trained and then optimized to return the greatest financial gains for the Algorithmic Trading Strategy that I have used.

- Baseline
First lets start with a summary of the Baseline model. The signals that I used to initiate a buy is (1) and a sell is (-1). We gave a signal of 1 to Actual Returns when they were equal to or greater than 0, and we gave a -1 to Actual Returns that were less than 0. We define Actual Returns as the percent change in closing price of whatever we are trading.
Using a rolling mean value with the rolling window set for 4 days gave me the Fast indicator and a rolling window of 100 days gave me a Slow indicator. These two indicators were my SMA indicators or Simple Moving Average indicators. They are the average price over the specified time period. We call them moving because they are plotted on a chart forming a line that moves with the average price change.

![SMA_plot](Resources/SMA_plot.png)

Here you can see the 2 Simple Moving Average indicators on the chart. Basically the trading strategy is when the percent change for the closing price goes up we buy in the hopes of the closing price continuing to go up, and when the percent change of the closing price goes down, we sell in the hopes that the price will continue to go down, taking advantage of the short term trends in price action.
A few parameters to note for the Baseline strategy are:
- SMA_Fast is set at 4 days
- SMA_Slow is set at 100 days
- Data for training the machine learning model was set at 3 months
- We used a SVM or Support Vector Method for its ability to discriminate between two classes, We wanted to be able to predict 1 or -1

## Results for Baseline

![baseline](Resources/pred_strategy_baseline.png)

Here you can see that the Strategy Returns (orange) outperformed the actual returns (blue). The Algorithmic trading bot was profitable and because the machine learning algorithim was able to predict with a decent accuracy of 55%, the future signal and trade accordingly, we were in profit.

- Version_2
For Version_2 I have tried to optimize the machine learning training dataset by extending the training time. Another way to put it is I have increased the amount of data that we let the model train with. The goal was to increase the accuracy of the model so that we could potentially make more money.
In the Baseline we gave the model 3 months of data to train with. In Version_2 we will give the model 6 months of training data and see what that results with.


