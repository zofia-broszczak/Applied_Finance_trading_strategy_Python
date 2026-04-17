# Applied_Finance_trading_strategy_Python
Volatility breakout trading strategy for EUR/PLN with GARCH-based volatility forecasting


## Project Overview
This repository contains a quantitative trading strategy developed for the Applied Finance course. The project focuses on implementing a volatility breakout strategy for the EUR/PLN currency pair, incorporating time-series volatility modeling and signal-based execution.

The full implementation, including methodology, analysis, and results, is provided in the Jupyter Notebook. The dataset used for the analysis is also included in this repository.

## Repository Structure
- **Applied Finance project 1- Broszczak Zofia.ipynb**  
  Main project file containing the complete implementation, analysis, and documentation.
  
- **eurpln-tick-2025-09-01-2025-10-06.csv**  
  Dataset used for model estimation and backtesting.
  
- **README.md**  
  Project description and summary.

## Strategy Description
The trading strategy is based on volatility breakout principles and includes the following components:

- GARCH(1,1) volatility model with an expanding estimation window and periodic refitting  
- One-step-ahead volatility forecasts used to construct dynamic price-scaled bands  
- Volatility bands calculated as forecasted volatility multiplied by lagged mid-price  
- Fast and slow EWMA signals for adaptive band construction  
- Liquidity filter based on spread thresholds (99th percentile)  
- Positioning logic that dynamically switches between momentum and mean-reversion regimes  

## Performance Metrics (Out-of-Sample)
- **Gross P&L:** 2807.0 PLN  
- **Net P&L:** 849.0 PLN  
- **Gross Sharpe Ratio:** 5.54  
- **Net Sharpe Ratio:** 1.64  
- **Number of Trades:** 29  

## Additional Information
All methodological details, intermediate steps, and outputs are documented within the Jupyter Notebook. The CSV file contains the raw EUR/PLN tick-level data used for the empirical analysis and backtesting.

---
