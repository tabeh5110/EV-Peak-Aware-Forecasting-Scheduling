# EV-Peak-Aware-Forecasting-Scheduling
Official repository for the manuscript: "Peak-Aware EV Charging-Station Load Forecasting and Constrained Scheduling Using an Adaptive Hybrid Ensemble"  This repository contains preprocessing, feature engineering, forecasting, uncertainty calibration, statistical validation, and constrained scheduling implementations.

Peak-Aware EV Charging-Station Load Forecasting and Constrained Scheduling Using an Adaptive Hybrid Ensemble
Overview

This repository contains the implementation and experimental outputs for the research study:

"Peak-Aware EV Charging-Station Load Forecasting and Constrained Scheduling Using an Adaptive Hybrid Ensemble"

The project presents an integrated forecast-to-schedule framework for electric vehicle (EV) charging infrastructure operation. The framework combines:

Leakage-free EV charging load forecasting
Adaptive Hybrid Peak-Aware Ensemble (E-AHPA)
Peak-Risk Calibrated E-AHPA (PRC-E-AHPA)
Validation-calibrated prediction intervals
Forecast-informed constrained EV charging scheduling

The objective is to improve short-term EV charging-load prediction while reducing operational risks associated with peak-load underestimation and capacity constraints.

Framework Components
1. Data Processing

The preprocessing pipeline converts raw EV charging records into hourly site-level load profiles.

Main operations:

Timestamp processing
Charging power aggregation
Site-level hourly load generation
Missing-hour handling
Chronological data preparation
2. Leakage-Free Feature Engineering

The feature pipeline generates forecasting variables using only historical information available before prediction time.

Feature groups include:

Calendar features
Cyclic time representations
Lag-memory features
Rolling historical statistics
Exponentially weighted memory features
Peak-risk memory features
Interaction features
Missing-value indicators
3. Forecasting Models

The repository implements:

Benchmark models
Linear Regression
LightGBM
CatBoost
XGBoost
Proposed models
E-AHPA

Adaptive Hybrid Peak-Aware Ensemble designed to balance:

Overall forecasting accuracy
Peak-risk behaviour
PRC-E-AHPA

Peak-Risk Calibrated E-AHPA designed to reduce:

Peak forecasting errors
High-load underestimation risk
4. Uncertainty Estimation

The framework includes validation-calibrated prediction intervals using conformal-style residual calibration.

The uncertainty component provides:

Upper-bound forecasts
Underestimation-risk reduction
Scheduling decision support
5. Constrained Scheduling

Forecast outputs are integrated into EV charging scheduling under:

Arrival-time constraints
Departure deadlines
Requested charging energy
Charger power limits
Site capacity constraints
Dataset Availability

The experiments use the publicly available:

Adaptive Charging Network (ACN) Dataset

provided by Caltech:

https://ev.caltech.edu/dataset

The raw ACN dataset is not redistributed in this repository because it remains subject to the original dataset provider's usage conditions.

This repository contains:

processed hourly load tables
engineered feature datasets
forecasting outputs
statistical validation results
scheduling experiment outputs
