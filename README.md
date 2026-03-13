# Dynamic Forecasting of Macroeconomic Time Series Using HVT

This repository contains R Markdown vignettes demonstrating **dynamic forecasting of macroeconomic time series data** using the [HVT (Hierarchical Vector Tessellation)](https://cran.r-project.org/package=HVT) package. It showcases the **MSM (Monte Carlo Simulation of Markov Chains)** feature for both ex-post and ex-ante forecasting, along with systematic hyperparameter experimentation for champion model selection.

---

## Vignettes

### 1. Dynamic Forecasting of Macroeconomic Data

**File:** `Dynamic_Forecasting_macroeconomic_data.Rmd`

End-to-end walkthrough of the MSM dynamic forecasting workflow:

- **Data Preparation** — Loading and preprocessing macroeconomic indicators (Dec 1998 – Sep 2025)
- **Feature Transformation** — 12-month log-differenced rate of change for standardization
- **HVT Model Training** — Hierarchical Vector Quantization for data compression and topology-preserving maps
- **MSM Forecasting** — Monte Carlo simulation of Markov chains for state-based time series prediction
- **Ex-post Validation** — Backtesting forecasts against historical data
- **Ex-ante Forecasting** — Forward-looking predictions using raw series 12-month direct lookback
- **Evaluation** — Forecast accuracy assessment using MAE and visual diagnostics

**Authors:** Zubin Dowlaty, Chepuri Gopi Krishna, Siddharth Shorya, Vishwavani

### 2. Hyperparameter Experimentation for Champion Model Selection

**File:** `Experimentation_of_hyperparameters_in_msm.Rmd`

Systematic grid search over key MSM hyperparameters to identify the optimal model configuration:

- **Parameters Explored:**
  - Number of cells in `trainHVT` (data compression granularity)
  - Number of clusters `k` (2–15 range recommended)
  - Number of nearest neighbors `nn` (for handling problematic states)
- **Evaluation Metric:** MAE (Mean Absolute Error) across all variables
- **Goal:** Identify the parameter combination yielding the lowest MAE for champion model selection

**Authors:** Zubin Dowlaty, Srinivasan Sundarsanam, Vishwavani Ravichandran, Nithya Sridhar

---

## Project Structure

```
testing-project/
├── Dynamic_Forecasting_macroeconomic_data.Rmd    # Main forecasting vignette
├── Dynamic_Forecasting_macroeconomic_data.html    # Rendered HTML report
├── Experimentation_of_hyperparameters_in_msm.Rmd  # Hyperparameter tuning vignette
├── Experimentation_of_hyperparameters_in_msm.html  # Rendered HTML report
└── README.md
```

---

## Requirements

### R Packages

```r
install.packages(c("dplyr", "tidyr", "xts", "patchwork", "feather", "ggplot2",
                   "kableExtra", "htmltools", "plotly", "tibble", "purrr",
                   "gganimate", "DT", "readr", "NbClust", "HVT"))
```

### HVT Package Version

- **HVT >= 25.2.8** is required for the full feature set (raw series ex-ante forecasting)
- Install from CRAN: `install.packages("HVT")`

### Dataset

The vignettes expect macroeconomic CSV datasets in a `sample_dataset/` folder. Ensure the data files are placed there before knitting.

---

## Usage

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Vishwavani-00/testing-project.git
   cd testing-project
   ```

2. **Open in RStudio** and knit either `.Rmd` file, or render from the command line:
   ```r
   rmarkdown::render("Dynamic_Forecasting_macroeconomic_data.Rmd")
   rmarkdown::render("Experimentation_of_hyperparameters_in_msm.Rmd")
   ```

3. **View the pre-rendered HTML reports** directly in a browser — no R installation required.

---

## Key Concepts

| Concept | Description |
|---------|-------------|
| **HVT** | Hierarchical Vector Tessellation — topology-preserving maps for multivariate data analysis |
| **HVQ** | Hierarchical Vector Quantization — data compression via hierarchical clustering |
| **MSM** | Monte Carlo Simulation of Markov Chains — state-based dynamic forecasting |
| **Voronoi Tessellation** | Partitioning projected space into distinct cells for hierarchical visualization |
| **Rate of Change** | `log(current) - log(12-month lag)` — standardizes features to comparable scale |

---

## License

Please refer to the repository for licensing information.
