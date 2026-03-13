# Testing Project — HVT Dynamic Forecasting Vignettes

This repository contains R Markdown vignettes demonstrating **Dynamic Forecasting** and **Hyperparameter Tuning** workflows using the [HVT (Hierarchical Vector Quantization)](https://github.com/Mu-Sigma/HVT) R package.

## Contents

| File | Description |
|------|-------------|
| `Dynamic_Forecasting_macroeconomic_data.Rmd` | End-to-end dynamic forecasting of macroeconomic time-series data using HVT's Markov State Model (MSM) |
| `Experimentation_of_hyperparameters_in_msm.Rmd` | Systematic hyperparameter tuning (grid search) over cells, clusters, and nearest neighbors to identify the champion MSM model |
| `*.html` | Pre-rendered HTML reports for each vignette |

## Key Concepts

- **Hierarchical Vector Quantization (HVQ)** — Compresses high-dimensional time-series data into topology-preserving cells
- **Markov State Model (MSM)** — Monte Carlo simulations over transition probability matrices for ex-post and ex-ante forecasting
- **Hyperparameter Optimization** — Automated grid search via `HVTMSMoptimization` across number of cells, clusters (k), and nearest neighbors (nn) to minimize MAE

## Dataset

The vignettes use a macroeconomic dataset (`sample_dataset/macro_raw_model_inputs_v5.csv`) spanning December 1998 to September 2025, featuring indicators such as:

- CPI, Coincident Index, Unemployment Rate
- S&P 500 ETF, Copper ETF, Oil Prices
- Treasury Yields, High Yield Spreads
- Sector ETFs (XLY, XLP, XLE, XLF, XLV, XLI, XLB)

## Prerequisites

- **R** (≥ 4.0)
- Required packages: `HVT`, `dplyr`, `xts`, `DT`, `plotly`

Install dependencies:

```r
install.packages(c("HVT", "dplyr", "xts", "DT", "plotly"))
```

## Usage

Open either `.Rmd` file in RStudio and knit to HTML, or render from the command line:

```r
rmarkdown::render("Dynamic_Forecasting_macroeconomic_data.Rmd")
rmarkdown::render("Experimentation_of_hyperparameters_in_msm.Rmd")
```

## Authors

- Zubin Dowlaty
- Srinivasan Sundarsanam
- Vishwavani Ravichandran
- Nithya Sridhar
- Chepuri Gopi Krishna
- Siddharth Shorya

## License

This project is for testing and demonstration purposes.
