# Machine Learning Algorithmic Trader with Python

![image](https://github.com/user-attachments/assets/ca9e4c77-539f-46a1-a9f3-3972190831f4)


## Overview
This project performs stock market analysis using historical stock data, technical indicators, and machine learning techniques to optimize a portfolio of stocks. The goal is to identify the best-performing stocks based on various criteria and create an optimized portfolio that maximizes returns while managing risk.

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Formulas Used](#formulas-used)
- [Strategies Used](#strategies-used)
- [Installation](#installation)

## Features
- Download historical stock data for S&P 500 companies.
- Calculate various technical indicators, including:
  - Garman-Klass Volatility
  - Relative Strength Index (RSI)
  - Bollinger Bands
  - Average True Range (ATR)
  - Moving Average Convergence Divergence (MACD)
- Perform K-means clustering to categorize stocks.
- Optimize portfolio weights using the Efficient Frontier method.
- Generate and plot cumulative returns for the optimized portfolio.

## Technologies Used
- **Python**: The primary programming language for data analysis and visualization.
- **Pandas**: A powerful data manipulation and analysis library used to handle and analyze stock data.
- **NumPy**: A library for numerical computations, enabling efficient mathematical operations on large datasets.
- **Matplotlib**: A plotting library used to visualize data and results through various types of charts and graphs.
- **Statsmodels**: A library for statistical modeling, allowing for the implementation of various statistical tests and models.
- **scikit-learn**: A machine learning library that provides tools for clustering (K-means) and other machine learning algorithms.
- **PyPortfolioOpt**: A library designed for portfolio optimization, implementing methods such as Mean-Variance Optimization and the Efficient Frontier.
- **yfinance**: A library for fetching historical market data from Yahoo Finance.
- **pandas-ta**: A library providing a collection of technical analysis indicators, making it easier to compute various stock metrics.

## Formulas Used
- **Garman-Klass Volatility**: 
  \[
  \sigma_{GK} = \sqrt{\frac{1}{2} \left( \ln\left(\frac{H}{L}\right) + 2 \ln\left(\frac{C}{O}\right) \right)}
  \]
  where \(H\), \(L\), \(C\), and \(O\) are the high, low, close, and open prices, respectively.

- **Relative Strength Index (RSI)**:
  \[
  RSI = 100 - \frac{100}{1 + RS}
  \]
  where \(RS\) is the average gain of up periods during the specified time frame divided by the average loss of down periods.

- **Bollinger Bands**:
  \[
  Upper Band = MA + (k \cdot \sigma)
  \]
  \[
  Lower Band = MA - (k \cdot \sigma)
  \]
  where \(MA\) is the moving average, \(\sigma\) is the standard deviation, and \(k\) is typically set to 2.

- **Average True Range (ATR)**:
  \[
  ATR = \text{average of True Range over n periods}
  \]
  where True Range is defined as the maximum of:
  - Current high - current low
  - Current high - previous close
  - Current low - previous close

- **Moving Average Convergence Divergence (MACD)**:
  \[
  MACD = EMA_{12} - EMA_{26}
  \]
  where \(EMA\) is the exponential moving average calculated over different periods.

## Strategies Used
- **K-means Clustering**: Used to group stocks based on their performance metrics, helping identify stocks with similar behaviors and performance patterns. This aids in diversification and understanding market segments.

- **Efficient Frontier**: Implemented to optimize the portfolio by identifying the best combination of stocks that provide the highest expected return for a given level of risk. This strategy helps to balance risk and reward by analyzing the trade-offs between different portfolio compositions.

- **Cumulative Returns Analysis**: The project calculates and visualizes the cumulative returns of the optimized portfolio compared to a benchmark (e.g., S&P 500) to evaluate performance effectively.

## Installation
To set up this project, ensure you have Python 3.x installed. You can install the necessary libraries using pip:

```bash
pip install pandas numpy matplotlib statsmodels scikit-learn PyPortfolioOpt yfinance pandas-ta
