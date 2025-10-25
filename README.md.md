# VaR Toolkit — Reusable Risk Analysis

**Purpose**: A concise, reusable notebook to compute **VaR (Parametric / Historical / Monte Carlo)**, **ES**, and **backtesting**.  
**Default data source**: `yfinance` (no token). Also supports **TuShare** (token) and **CSV** (fallback).

## Quick Start
1. Open `VaR_toolkit_yf.ipynb`.
2. In section **0. Parameters**, set:
   - `SYMBOL` (e.g., `600036.SS`, `AAPL`, `0700.HK`)
   - `START` / `END`
   - `DATA_SOURCE = "yfinance"` (default) or `"tushare"` or `"csv"`
   - If using TuShare, set your token in environment:  
     - Create `.env` with `TUSHARE_TOKEN=YOUR_TOKEN`, or  
     - `setx TUSHARE_TOKEN "YOUR_TOKEN"` (Windows) / `export TUSHARE_TOKEN=YOUR_TOKEN` (macOS/Linux).
3. Run all cells. Figures will be saved to `./figures/`, summary to `./outputs/summary.csv`.

## Outputs
- `figures/return_distribution.png`
- `figures/rolling_vol.png`
- `figures/var_comparison_1d_95.png`
- `outputs/summary.csv`

## Notes
- Parametric VaR uses normal approximation; consider tail risk.
- Historical VaR is sensitive to sample length.
- Monte Carlo VaR depends on distributional assumptions.
