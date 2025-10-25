# 📊 Financial Risk Analysis — VaR Toolkit  
**by Lyra**

![VaR Toolkit Cover](./figures/var_comparison_1d_95.png)

---

## 📌 Overview
A **reusable Value-at-Risk (VaR) toolkit** built for financial engineers and analysts.  
The notebook implements **Parametric**, **Historical Simulation**, and **Monte Carlo** VaR models,  
along with **Expected Shortfall (ES)** and **basic backtesting**, using `yfinance` as the default data source.

It is designed for **real-world research**, not just coursework — adaptable, lightweight, and fully reproducible.

---

## ⚙️ Key Features
- 🧩 **Modular design** — change only symbol or date window to reuse.  
- 🌐 **Default: yfinance**, optional TuShare or CSV fallback.  
- 📈 **Three VaR models** — Parametric, Historical Simulation, Monte Carlo.  
- 📉 **Expected Shortfall (ES)** calculation and annualized metrics.  
- 🔍 **Backtesting** — 95% exceedance frequency by year.  
- 🧮 **Auto-export** — results → `outputs/summary.csv`, figures → `figures/`.  
- 💼 **Practical tone** — clean codebase, built for portfolio use.

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
   ```
4. Run all cells.  

Results will automatically generate:  
```
./figures/return_distribution.png  
./figures/rolling_vol.png  
./figures/var_comparison_1d_95.png  
./outputs/summary.csv
```

> 🧠 **Tip:**  
> If using TuShare, create `.env` and set your token:
> ```
> TUSHARE_TOKEN=your_token_here
> ```

---

## 📊 Example Outputs
| Figure | Description |
|:--|:--|
| **Return Distribution** | Empirical vs. normal fit; identifies fat tails. |
| **Rolling Volatility** | Annualized 60-day volatility trend. |
| **VaR Comparison** | Overlay of Parametric / Historical / Monte Carlo 1-day 95% VaR. |
| **Backtesting Table** | Annual exceedance count and ratio vs theoretical 5%. |

---

## 🧠 Interpretation Notes
- **Parametric VaR** assumes normality — may underestimate tail risk.  
- **Historical VaR** depends on sample window; adaptive to empirical shocks.  
- **Monte Carlo VaR** reflects distribution assumptions — flexible but model-dependent.  
- **Backtesting** validates calibration — 95% VaR ≈ 5% exceedance expectation.

---

## 🧩 Folder Structure
```
Financial-Risk-Analysis-VaR/
├─ VaR_toolkit_yf.ipynb
├─ README.md
├─ .gitignore
├─ .gitattributes
├─ env.example
├─ figures/
│   └─ var_comparison_1d_95.png
└─ outputs/
    └─ summary.csv
```

---

## 🔒 Security Notice
Never upload your personal `.env` file — it may contain private API tokens.  
Keep only `.env.example` for reference.

---

## 📚 Requirements
```
pandas  
numpy  
matplotlib  
scipy  
yfinance  
tushare (optional)
```

---

## 🧾 License
MIT License © Lyra  
You are free to use, modify, and share this project with attribution.

---

## 🌐 About
Built by **Lyra**,  
as part of an independent financial engineering toolkit initiative —  
focusing on practical, reproducible, and visually clear risk analytics.
