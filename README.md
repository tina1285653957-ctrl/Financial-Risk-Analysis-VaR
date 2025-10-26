#  Financial Risk Analysis — VaR Toolkit  
**by Lyra**

<p align="center">
  <img src=".\figures\cover.png.png" alt="VaR Toolkit Cover" width="750"/>
</p>

---

##  Overview

A **reusable Value-at-Risk (VaR) toolkit** built for financial engineers and analysts.  
The notebook implements **Parametric**, **Historical Simulation**, and **Monte Carlo** VaR models,  
along with **Expected Shortfall (ES)** and **basic backtesting**, using `yfinance` as the default data source.

It is designed for **real-world research**, lightweight, and fully reproducible.

这是一个**可复用的 VaR 分析工具包**，为金融工程师与风险分析师提供便利。  
运用Notebook 实现 **参数法**、**历史模拟法**、  以及 **蒙特卡洛法** 三种 VaR 模型，  同时支持 **期望损失** 与 **回测**。
项目默认数据源为 `yfinance`，也支持 **TuShare（需 Token）** 与 **本地 CSV 文件**，  
结构清晰、轻量化，可用于真实金融场景下的风险研究、教学与量化建模。

---

##  Key Features
-  **Modular design** — change only symbol or date window to reuse.  
-  **Default: yfinance**, optional TuShare or CSV fallback.  
-  **Three VaR models** — Parametric, Historical Simulation, Monte Carlo.  
-  **Expected Shortfall (ES)** calculation and annualized metrics.  
-  **Backtesting** — 95% exceedance frequency by year.  
-  **Auto-export** — results → `outputs/summary.csv`, figures → `figures/`.  
-  **Practical tone** — clean codebase, built for portfolio use.

- **模块化**：只用修改股票代码或时间区间，就可以复用。  
- **默认数据源 yfinance**：可选 TuShare 或 CSV。  
- **三种 VaR 模型**：参数法、历史模拟法、蒙特卡洛法。  
- **支持 ES 指标**：用来衡量极端风险下的预期损失。  
- **回测功能**：展示 95% 置信区间下的年度超越次数与比例。  
- **导出结果并存储**：分析数据保存至 `outputs/summary.csv`，图像保存至 `figures/`。  
- **实战取向**：代码比较简洁、适合用于项目作品集或投研分析展示。
---

##  Quick Start
1. Clone this repository or download the notebook.  
2. Open `VaR_toolkit_yf.ipynb` in Jupyter / VS Code.  
3. In section **0. Parameters**, edit:
   ```python
   SYMBOL = "600036.SS"      # or AAPL, 0700.HK, etc.
   START  = "2018-01-01"
   END    = "2025-01-01"
   DATA_SOURCE = "yfinance"  # or "tushare" / "csv"
