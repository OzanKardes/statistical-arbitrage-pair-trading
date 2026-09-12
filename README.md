# Statistical Arbitrage & Pair Trading

## Overview

This project investigates whether statistically related equity pairs exhibit
persistent mean-reversion that can be exploited through a market-neutral
statistical arbitrage strategy.

The analysis was implemented in Python using historical equity data from
Yahoo Finance.

## Methodology

The project:

- Screens 120 equity pairs
- Tests return correlation
- Applies Engle-Granger cointegration tests
- Estimates hedge ratios using OLS regression
- Constructs mean-reverting spreads
- Generates z-score-based trading signals
- Builds a market-neutral long/short portfolio
- Incorporates transaction costs
- Performs strict out-of-sample testing
- Performs parameter sensitivity analysis

## Data

Historical adjusted equity prices were obtained using `yfinance`.

Universe:
- Mastercard (MA)
- Visa (V)
- JPMorgan (JPM)
- Walmart (WMT)
- Coca-Cola (KO)
- PepsiCo (PEP)
- and other liquid US equities

## Results

The strongest candidate identified during the screening process was
Mastercard / Visa, with an Engle-Granger cointegration p-value of approximately
0.010.

The final strategy was evaluated out-of-sample using parameters estimated
exclusively from 2021–2024 and tested on 2025 data.

The out-of-sample results demonstrated limited persistence of the historical
mean-reversion relationship, highlighting the importance of parameter
stability, transaction costs and avoiding look-ahead bias.

## Key Concepts

- Statistical arbitrage
- Cointegration
- Mean reversion
- OLS hedge ratios
- Z-scores
- Market-neutral portfolios
- Out-of-sample testing
- Transaction-cost modelling
- Robustness testing

## Technologies

Python  
NumPy  
Pandas  
Statsmodels  
yfinance  
Matplotlib
