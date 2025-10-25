# 📊 Financial Risk Analysis — VaR Toolkit  
**by Lyra**

<p align="center">
  <img src="./figures/cover.png" alt="VaR Toolkit Cover" width="750"/>
</p>

---

## 📌 Overview
A **reusable Value-at-Risk (VaR) toolkit** built for financial engineers and analysts.  
The notebook implements **Parametric**, **Historical Simulation**, and **Monte Carlo** VaR models,  
along with **Expected Shortfall (ES)** and **basic backtesting**, using `yfinance` as the default data source.

It is designed for **real-world research**, not just coursework — adaptable, lightweight, and fully reproducible.

---

## ⚙️ Key Features
-  **Modular design** — change only symbol or date window to reuse.  
-  **Default: yfinance**, optional TuShare or CSV fallback.  
-  **Three VaR models** — Parametric, Historical Simulation, Monte Carlo.  
-  **Expected Shortfall (ES)** calculation and annualized metrics.  
-  **Backtesting** — 95% exceedance frequency by year.  
-  **Auto-export** — results → `outputs/summary.csv`, figures → `figures/`.  
-  **Practical tone** — clean codebase, built for portfolio use.

---

## 🚀 Quick Start
1. Clone this repository or download the notebook.  
2. Open `VaR_toolkit_yf.ipynb` in Jupyter / VS Code.  
3. In section **0. Parameters**, edit:
   ```python
   SYMBOL = "600036.SS"      # or AAPL, 0700.HK, etc.
   START  = "2018-01-01"
   END    = "2025-01-01"
   DATA_SOURCE = "yfinance"  # or "tushare" / "csv"
