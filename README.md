# Dynamic Forecasting & Hyperparameter Experimentation using HVT

Research experiments on **dynamic forecasting of macroeconomic time series** and **hyperparameter tuning for champion model selection** using Hierarchical Vector Tiling (HVT) and Markov Switching Models (MSM).

---

## 📋 Overview

This repository contains two R Markdown vignettes that demonstrate end-to-end workflows for:

1. **Dynamic Forecasting of Macroeconomic Data** — Applying HVT-based methods to macroeconomic time series for multi-step-ahead forecasting with interactive visualizations.
2. **Hyperparameter Experimentation for MSM** — Systematic experimentation of hyperparameters to identify champion models in Markov Switching Model-based dynamic forecasting.

Both vignettes include rendered HTML outputs for easy viewing without requiring an R environment.

---

## 📁 Repository Structure

```
testing-project/
├── Dynamic_Forecasting_macroeconomic_data.Rmd    # Vignette 1: HVT-based dynamic forecasting
├── Dynamic_Forecasting_macroeconomic_data.html    # Rendered output (interactive, viewable in browser)
├── Experimentation_of_hyperparameters_in_msm.Rmd # Vignette 2: Hyperparameter experimentation
├── Experimentation_of_hyperparameters_in_msm.html # Rendered output (interactive, viewable in browser)
└── README.md
```

---

## 📊 Vignette 1: Dynamic Forecasting of Macroeconomic Time Series using HVT

**Authors:** Zubin Dowlaty, Chepuri Gopi Krishna, Siddharth Shorya, Vishwavani

Applies Hierarchical Vector Tiling (HVT) to macroeconomic time series data for dynamic forecasting. The vignette covers:

- Data preparation and exploratory analysis of macroeconomic indicators
- HVT-based hierarchical clustering and tiling
- Multi-step-ahead dynamic forecasting
- Interactive Plotly visualizations and heatmaps
- Model evaluation and performance metrics

**View:** Open `Dynamic_Forecasting_macroeconomic_data.html` in any browser.

---

## 🔬 Vignette 2: Hyperparameter Experimentation for Champion Model Selection in MSM

**Authors:** Zubin Dowlaty, Srinivasan Sundarsanam, Vishwavani Ravichandran, Nithya Sridhar

Systematic experimentation of hyperparameters for Markov Switching Model (MSM) based dynamic forecasting. The vignette covers:

- Hyperparameter grid design and search strategy
- Model training across parameter combinations
- Champion model selection criteria and evaluation
- Comparative analysis of model configurations
- Performance benchmarking and result visualization

**View:** Open `Experimentation_of_hyperparameters_in_msm.html` in any browser.

---

## 🛠️ Prerequisites

To run the `.Rmd` files locally:

- **R** (≥ 4.0)
- **RStudio** (recommended)
- Required R packages:
  ```r
  install.packages(c("rmarkdown", "knitr", "plotly", "dplyr", "ggplot2"))
  ```
  Additional domain-specific packages (HVT, MSM libraries) will be noted within each vignette.

---

## 🚀 Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Vishwavani-00/testing-project.git
   cd testing-project
   ```

2. **View rendered outputs** (no R required):
   Open the `.html` files directly in your browser.

3. **Re-run the analysis** (requires R):
   Open any `.Rmd` file in RStudio and click **Knit**, or run:
   ```r
   rmarkdown::render("Dynamic_Forecasting_macroeconomic_data.Rmd")
   rmarkdown::render("Experimentation_of_hyperparameters_in_msm.Rmd")
   ```

---

## 📖 Key Concepts

| Concept | Description |
|---------|-------------|
| **HVT** | Hierarchical Vector Tiling — a hierarchical clustering method for partitioning high-dimensional data into interpretable tiles |
| **MSM** | Markov Switching Models — regime-switching models that capture structural changes in time series dynamics |
| **Dynamic Forecasting** | Multi-step-ahead forecasting where each forecast step uses the predicted (not actual) values from prior steps |
| **Champion Model** | The best-performing model configuration selected through systematic hyperparameter experimentation |

---

## 👥 Authors

- **Zubin Dowlaty**
- **Chepuri Gopi Krishna**
- **Siddharth Shorya**
- **Vishwavani Ravichandran**
- **Srinivasan Sundarsanam**
- **Nithya Sridhar**

---

## 📄 License

This project is for research and educational purposes. Please refer to individual vignettes for data attribution and usage terms.
