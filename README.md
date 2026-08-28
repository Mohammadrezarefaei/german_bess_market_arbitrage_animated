## 🔋 Advanced BESS Asset Optimization & Arbitrage (DE/LU Market)
This project moves beyond simple data visualization to implement a mathematically rigorous **Linear Programming (LP)** optimization model for Battery Energy Storage Systems (BESS) using 15-minute resolution data from SMARD.de.

### 🚀 Key Features
- **Data Engineering:** Automated pipeline for loading, cleaning, and parsing quarter-hourly German day-ahead electricity prices.
- **Mathematical Optimization (PuLP):** Formulated an LP model respecting physical constraints:
  - State of Charge (SoC) continuity across time steps ($t-1$ to $t$).
  - Power capacity limits ($P_{max}$) and energy capacity bounds ($E_{cap}$).
  - Round-trip efficiency ($\eta = 85\%$).
- **Dark-Mode Visualizations & Animations:** Dynamic GIF rendering to visualize charging/discharging dispatch patterns over time.

### 📊 Results Snapshot
- **Total LP Optimized Arbitrage Profit:** ~2,346 € (across simulated test period)
- **Average Daily Net Profit:** ~213 € / day (for a 1MW / 2MWh asset)
