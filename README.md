# Algorithmic Trading Strategy on SPY using GA-Optimized Indicators and LSTM

## Overview
This repository contains a team MSc project focused on building and evaluating a prediction-based trading strategy for the SPDR S&P 500 ETF Trust (SPY).

The project combines:
- historical market data from Yahoo Finance
- feature engineering with technical indicators such as MACD, RSI, and EMA
- genetic algorithm (GA) optimization of indicator parameters
- LSTM-based next-day price prediction
- backtesting against benchmark strategies

## Project Type
Team project

## My Contribution
My primary contribution focused on:
- data extraction from Yahoo Finance
- preprocessing and cleaning time-series data
- feature engineering using technical indicators, including MACD and RSI
- preparing the structured dataset for downstream modelling

## Objective
The goal of the project was to test whether machine learning and optimized technical indicators could be combined to create a practical rule-based trading strategy for SPY.

## Methodology
1. Downloaded SPY market data for January 2021 to January 2026.
2. Cleaned and chronologically structured the time-series dataset.
3. Engineered features including returns, EMA, RSI, MACD, volatility-related variables, and volume-based signals.
4. Applied a genetic algorithm to optimize technical-indicator parameters using training data only.
5. Trained an LSTM model to predict next-day closing prices.
6. Converted predictions into buy/sell/hold trading signals.
7. Backtested the strategy against buy-and-hold and random trading benchmarks.

## Tools Used
- R
- R Markdown
- quantmod
- TTR
- dplyr
- ggplot2
- GA
- keras

## Key Results
Using an initial capital of 10,000:
- Prediction-based strategy final value: 10,817.40
- Total return: 8.17%
- Annualized return: 8.49%
- Volatility: 15.76%
- Sharpe ratio: 0.47
- Max drawdown: -14.77%
- Win rate: 57.14%
- Number of trades: 7

Benchmark comparison:
- Buy-and-hold final value: 11,474.73
- Buy-and-hold total return: 14.75%
- Random strategy final value: 10,618.71
- Random strategy total return: 6.19%

## Interpretation
The prediction-based strategy outperformed the random trading benchmark, suggesting useful predictive signal, but it underperformed a simple buy-and-hold strategy during a strongly bullish test period. This highlights both the value and the limitations of model-based trading systems in trending markets.

## Repository Structure
- `src/algorithmic-trading.Rmd` — full modelling and backtesting workflow
- `report/algorithmic-trading-report.pdf` — final report

## Notes
This repository is shared for academic and portfolio purposes.
