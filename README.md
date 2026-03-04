# Multi-Source Financial Time Series Analyzer

A unified Python framework for analyzing financial time series across **Yahoo Finance**, **Alpha Vantage**, and **Binance**. This project standardizes market data from multiple providers into a single analytics pipeline for computing returns, volatility, risk-adjusted performance, tail-risk metrics, and comparative asset diagnostics.

## Overview

This project was built to provide a reusable and extensible foundation for **quantitative financial analysis**. Rather than writing separate logic for each data vendor, it uses a single data-loading abstraction that normalizes price data from multiple sources before applying a shared analytics workflow.

The result is a flexible tool for exploring:
- asset returns
- realized volatility
- drawdowns
- Sharpe and Sortino ratios
- Value at Risk (VaR) and Conditional Value at Risk (CVaR)
- cross-asset correlation

It is designed as a practical introduction to **quantitative research workflows**, including data ingestion, preprocessing, statistical analysis, and visualization.

## Features

- Unified support for:
  - **Yahoo Finance**
  - **Alpha Vantage**
  - **Binance**
- Standardized close-price extraction across providers
- Arithmetic and logarithmic return calculation
- Cumulative return analysis
- Rolling annualized volatility
- Rolling Sharpe ratio
- Drawdown tracking and maximum drawdown
- Historical **VaR** and **CVaR**
- Correlation matrix generation
- Multi-asset comparison
- Built-in visualizations for return and risk diagnostics

## Supported Data Sources

### Yahoo Finance
Best suited for equities, ETFs, and broad market instruments.

### Alpha Vantage
Useful for equity time series with adjusted daily data. Requires an API key.

### Binance
Supports crypto market data using exchange-native symbols such as `BTCUSDT` and `ETHUSDT`.

## Metrics Implemented

The analytics pipeline currently includes:

- **Arithmetic Returns**
- **Log Returns**
- **Cumulative Returns**
- **Annualized Return**
- **Annualized Volatility**
- **Sharpe Ratio**
- **Sortino Ratio**
- **Rolling Volatility**
- **Rolling Sharpe**
- **Drawdown Series**
- **Maximum Drawdown**
- **Historical VaR**
- **Historical CVaR**
- **Correlation Matrix**

## Project Structure

```bash
.
├── market_data_analyzer.py   # Main script containing loaders, analytics, and plots
├── README.md                 # Project documentation
└── requirements.txt          # Project dependencies (optional)
