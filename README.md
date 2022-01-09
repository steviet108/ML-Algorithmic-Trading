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

First lets start with a summary of the Baseline model. The signals that I used to initiate a buy is (1) and a sell is (-1). Using a rolling mean value with the rolling window set for 4 days gave me the Fast indicator and a rolling window of 100 days gave me a Slow indicator. These two indicators were my SMA indicators or Simple Moving Average indicators. They are the average price over the specified time period. We call them moving because they are plotted on a chart forming a line that moves with the average price change.

![SMA_plot](Resources/SMA_plot.png)








