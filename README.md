# Solar Generation Forecasting Baselines for Grid Operations

## Problem Statement
High penetration of solar PV introduces variability and uncertainty that directly affects grid operations, particularly in power systems with limited flexibility and reserves.

Accurate solar generation forecasting is therefore critical not only for energy estimation, but for operational reliability.

## Objective
This repository develops and evaluates baseline solar generation forecasting models with a focus on metrics and behaviors relevant to power system operations.

The work prioritizes:
- Reproducibility
- Transparency of assumptions
- Robustness under data-scarce and high-variability conditions

## Scope
- Short-term solar generation forecasting
- Evaluation using RMSE, MAE, and MAPE
- Emphasis on operational relevance rather than model complexity

## Context
Methods are designed to be globally applicable and are validated using conditions representative of emerging and weak-grid power systems as stress-test cases.

## Status
Project initialized. Baseline models and datasets will be added incrementally.

---

## Data Source
Solar irradiance and temperature data are obtained from the NASA POWER project
(hourly, satellite/reanalysis-based estimates).

Primary variables:
- Global Horizontal Irradiance (ALLSKY_SFC_SW_DWN)
- Ambient Temperature at 2m (T2M)

Location:
- Maroua, Cameroon (Sahelian stress-test environment)

See `data/README.md` for full data documentation, missingness, and limitations.

---

## Repository Structure

```text
notebooks/
  00_data_preparation.ipynb        Data cleaning + quality checks
  01_persistence_baseline.ipynb    Persistence benchmark forecast
  02_statistical_baseline.ipynb    Simple regression / random forest baseline

data/
  README.md                        Dataset provenance + quality metrics
  Dataset_phase_1.csv              Raw NASA POWER export
  Dataset_phase_1_clean.csv        Cleaned dataset used for modeling
