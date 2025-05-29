# Technical Analysis and Trading Strategy Backtester

A Python-based system to analyze NSE stock prices, calculate technical indicators, backtest an RSI-based trading strategy, and visualize results in a SEBI-compliant dashboard. Built to align with NISM Series XV (Research Analyst) certification requirements.

## Overview
This project analyzes historical data for 5 NSE stocks (TCS, RELIANCE, SBIN, INFY, HDFCBANK) from Jan 2024 to May 2025. It calculates technical indicators (RSI, MACD, Bollinger Bands), backtests an RSI-based strategy (buy when RSI < 30, sell when RSI > 70), and compares performance to the NIFTY 50 benchmark. Results are visualized in a Flask dashboard with SEBI-compliant reporting.

## Features
- **Data Fetching**: Uses `yfinance` to fetch NSE stock and NIFTY 50 data.
- **Technical Indicators**: Computes RSI, MACD, and Bollinger Bands using `ta` library.
- **Backtesting**: Implements an RSI-based trading strategy with ₹100,000 initial capital per stock.
- **Visualization**: Flask dashboard displays indicator plots and strategy returns.
- **SEBI Compliance**: Includes a compliance note per SEBI (Research Analysts) Regulations, 2014.
- **Database**: Stores data in MSSQL Server Express for efficient querying.

## Project Structure
- `sql/`: MSSQL scripts for database setup (`setup_database.sql`, `setup_indicators_table.sql`).
- `src/`: Python scripts for data fetching (`fetch_data.py`), indicator calculation (`calculate_indicators.py`), and backtesting (`backtest_strategy.py`).
- `dashboard/`: Flask app (`app.py`), HTML templates (`templates/`), and static files (`static/`).
- `requirements.txt`: Python dependencies.

## Setup and Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Que-sh/Technical-Analysis-Backtester.git
   cd Technical-Analysis-Backtester
