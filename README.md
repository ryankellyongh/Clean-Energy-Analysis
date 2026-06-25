# Clean-Energy-Analysis

This project analyzes annual U.S. energy generation by source from 2014 to 2024 using data imported from the U.S. Energy Information Administration (EIA).”
“The purpose of this analysis is to examine how major energy sources have changed over time, compare fossil fuel and renewable energy patterns, and evaluate whether there are clear linear trends.

## Project Overview
This repository contains an analytical study of U.S. energy generation trends from 2014–2024.
The project evaluates long‑term changes in major energy sources and tests for statistically significant trends that indicate a transition toward renewable and low‑carbon energy.

## The analysis includes:

- Descriptive statistics

- Distribution analysis (histograms, boxplots)

- Time‑series visualization

- Lag plots and ARIMA forecasting

- Linear regression modeling

- Model diagnostics and correlation analysis

## Dataset

The cleaned dataset includes the following variables:

- Year

- Coal

- Natural_Gas

- Nuclear

- Hydroelectric

- Solar

## Derived totals:

Fossil_Total = Coal + Natural_Gas

Renewable_Total = Hydroelectric + Solar

Low_Carbon_Total = Nuclear + Hydroelectric + Solar

The dataset contains no missing values and is ready for analysis.

## Research Questions

1. Are there statistically significant trends in U.S. energy generation over time?
2. Is there evidence of a transition from fossil fuels to renewable or low‑carbon energy sources?

## Methods

- Statistical Techniques

- Summary statistics

- Histograms and boxplots

- Time‑series line plots

- Lag analysis

- ARIMA forecasting (Solar)

Linear regression:
Y = β0 + β1(Year) + ε

## Significance Level

All hypothesis tests use α = 0.05

## Key Findings

Significant Trends (Reject H₀)

Coal — significant decline

Natural Gas — significant increase

Nuclear — small but significant trend

Solar — strong upward trend

Fossil Total — significant trend

Renewable Total — strong increase

Low Carbon Total — significant increase

No Significant Trend (Fail to Reject H₀)

Hydroelectric — stable with low variability

## Additional Insights

Solar shows nonlinear acceleration, confirmed by ARIMA(0,2,0).

Coal follows a stable linear decline with strong model fit.

Natural gas remains the largest contributor on average.

Renewable and low‑carbon totals show consistent growth, though fossil fuels still dominate overall generation.

Model Performance (R² Highlights)

Coal, Natural Gas, Solar: R² > 0.93

Renewable Total: R² ≈ 0.915

Low Carbon Total: R² ≈ 0.782

Fossil Total: R² ≈ 0.548

Hydroelectric: R² ≈ 0.122

## Repository Structure

data/

epa_03_01_a_cleaned.xlsx

figures/

histograms/

boxplots/

time_series/

lag_plots/

arima_forecast/

Clean Energy Analysis.Rmd

README.md


## How to Run the Analysis

Install required R packages:

r

install.packages(c(
  "readr", "dplyr", "tidyr", "ggplot2", "broom",
  "scales", "readxl", "knitr", "kableExtra",
  "tibble", "forecast"
))

Open Clean Energy Analysis.Rmd in RStudio.

Ensure the dataset is located at:

data/epa_03_01_a_cleaned.xlsx

Knit the R Markdown file to generate the full HTML report.

## Future Improvements

- Incorporate monthly EIA data for seasonality analysis

- Apply nonlinear models for solar and renewables

- Add policy scenario modeling

- Compare U.S. trends with international data
