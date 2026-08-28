```markdown
# German BESS Arbitrage & High-Frequency Price Optimization

A Python-based engineering toolkit designed to analyze 15-minute high-resolution power market data from the German/Luxembourg (DE/LU) bidding zone, model battery energy storage system (BESS) dispatch strategies, and visualize intraday volatility and arbitrage margins.

## Project Overview
In modern European power markets, relying on annual average price forecasts or flat baseline models fails to capture the true economics of flexible assets. This repository provides scripts to process real clearing prices from **SMARD.de** (the official data platform of the German Federal Network Agency) to highlight:
* **Midday Renewable Gluts:** Sub-zero and low pricing intervals driven by unconstrained solar over-generation.
* **Evening Scarcity Ramps:** Steep residual load peaks creating high-margin discharge opportunities.
* **Intraday Spreads vs. Degradation:** Simulating optimal dispatch boundaries beyond static baseline assumptions.

## Repository Structure
```text
├── data/
│   └── Day-ahead_prices_202608180000_202608290000_Quarterhour.csv  # SMARD raw export
├── assets/
│   └── german_bess_market_arbitrage_animated.gif                      # Visualized dispatch execution
├── notebooks/
│   └── bess_market_analysis.ipynb                                   # Jupyter notebook containing the full pipeline
└── README.md

```

## Core Features

* **SMARD Data Ingestion:** Robust parsing of quarter-hourly CSV exports with automatic handling of German locale decimal formats and timestamp indexes.
* **Non-linear Dispatch Logic:** Algorithmic identification of smart charging zones (low/negative pricing windows) and high-margin discharge spikes.
* **Advanced Visualization:** Dark-themed, publication-ready static charts and animated GIF generators using `matplotlib` and `matplotlib.animation`.

## Quick Start

1. Clone the repository and ensure Python 3.9+ is installed.
2. Install the required dependencies:
```bash
pip install pandas numpy matplotlib

```


3. Run the analysis notebook or script inside your environment to process the SMARD dataset and render the arbitrage execution curves.

## License

Distributed under the MIT License. See `LICENSE` for more information.

```

```
