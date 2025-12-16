# Options_Basics Notebooks

This repo contains self-contained Python notebooks exploring BTC options pricing, risk, and volatility surfaces. They are designed as teaching/analysis aids you can point to on a CV.

## Notebook Map
- `Options_Basics.ipynb` — Black–Scholes pricing and full Greeks; payoff and sensitivity visuals; time/vol/gamma risk tables; scenario-based P&L and Greek attribution for a BTC call portfolio.
- `atm_iv_term_structure.ipynb` — Deribit API pull of the live option book; cleans strikes/expiries; plots nearest-expiry IV smile and ATM IV term structure anchored to the BTC index price.
- `delta_hedging.ipynb` — Simulates delta-hedging a short BTC call with an autocorrelated price path; tracks hedge adjustments, option/hedge/net P&L, theta collected, and day-level reports.
- `votility_surface_01.ipynb` — Builds front-expiry smiles and full 3D implied-vol and total-variance surfaces (strike or log-moneyness vs DTE) from Deribit data, with grid interpolation and matplotlib visuals.

## Run Notes
- Python 3 with `pandas`, `numpy`, `matplotlib`, `seaborn`, `scipy`, and `requests` is sufficient. Install via `pip install pandas numpy matplotlib seaborn scipy requests`.
- The IV/vol-surface notebooks call the public Deribit API; you need network access for live data.
- Plots render inline in Jupyter; if running headless, use a compatible matplotlib backend (e.g., `Agg`).

Credit to VertoxQuant
