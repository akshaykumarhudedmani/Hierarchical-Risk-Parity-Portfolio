# Hierarchical Risk Parity (HRP) Portfolio Engine

**Event:** Arbitrage Arena 2026 | **Problem Statement:** Cross-Asset Survivability  
**Team:** Akshay Kumar & Vishruth

![Equity Curve](<img width="1189" height="607" alt="Screenshot 2026-01-04 184746" src="https://github.com/user-attachments/assets/f8124bd9-213d-4a86-826b-758ea3125389" />)

## Project Overview
This project implements a **Hierarchical Risk Parity (HRP)** model to optimize a cross-asset portfolio (Crypto, Equities, Commodities). Unlike traditional Mean-Variance optimization, HRP uses **Machine Learning Clustering** to allocate capital based on risk hierarchy rather than unstable return predictions.

**Key Achievement:**
The model successfully navigated the **2022 Inflation Crisis**, reducing Max Drawdown by **10%** compared to the NASDAQ Benchmark while maintaining a higher Sharpe Ratio (**0.77** vs 0.67).

## Key Features
* **No Look-Ahead Bias:** Implemented strict intersection logic to align 24/7 Crypto markets with Mon-Fri Equities data.
* **Regime Robustness:** Uses `scipy.cluster` to identify "Safe Haven" clusters (Gold/Silver) without human intervention.
* **Stress Testing:** Includes specific modules to backtest performance during the **COVID-19 Crash** and **2022 Rate Hike Cycle**.

## Tech Stack
* **Python 3.10+**
* **Pandas & NumPy:** Vectorized backtesting engine.
* **SciPy:** Dendrogram clustering and distance matrix calculations.
* **Matplotlib/Seaborn:** Financial visualization.

## Data & Usage
**Note:** The raw `.csv` datasets used for this competition are proprietary to Arbitrage Arena 2026 and are **not included** in this repository.

To run this notebook:
1.  Place standard OHLCV `.csv` files (e.g., `BTC_USD.csv`, `AAPL.csv`) in the root directory.
2.  Ensure filenames match the `file_map` dictionary in Cell 2.
3.  Run the notebook cells sequentially.

## License
This project is for educational and portfolio demonstration purposes.
