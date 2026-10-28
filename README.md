# Air Quality Analysis and PM2.5 Prediction in Ratnanagar, Nepal (2025)

**Author:** Bandana Dhakal  
**Study Area:** Ratnanagar, Chitwan, Nepal  
**Study Period:** January–December 2025

## Project Overview

This project investigates air-quality patterns in Ratnanagar, Nepal, using hourly modelled air-quality data obtained from the Open-Meteo Air Quality API.

It examines seasonal changes in particulate pollution, relationships between air pollutants, and the performance of machine-learning models for one-hour-ahead PM2.5 prediction.

## Research Objectives

1. Analyze PM2.5 and PM10 concentrations.
2. Examine monthly and seasonal pollution patterns.
3. Investigate relationships between pollutants.
4. Analyze variations in the US Air Quality Index (AQI).
5. Develop machine-learning models for next-hour PM2.5 prediction.
6. Evaluate model accuracy using unseen chronological test data.

## Dataset

- **Source:** Open-Meteo Air Quality API
- **Location:** Ratnanagar, Nepal
- **Period:** January 1–December 31, 2025
- **Records:** 8,760 hourly observations
- **Variables:** PM2.5, PM10, US AQI, nitrogen dioxide, and ozone
- **Missing values:** 0
- **Duplicate timestamps:** 0

The dataset consists of modelled air-quality estimates rather than direct measurements from a local monitoring station.

## Methodology

The analysis was performed using Python and Google Colab.

The workflow includes data collection, data cleaning, exploratory data analysis, feature engineering, chronological training/testing separation, model training, and performance evaluation.

Three forecasting approaches were compared:

- Persistence Baseline
- Linear Regression
- Random Forest Regression

Approximately 80% of the usable samples were allocated to training and 20% to testing.

## Results

### Air Quality Analysis

The estimated annual mean PM2.5 concentration was approximately **48.75 µg/m³**.

The monthly analysis showed higher PM2.5 concentrations during the early months of the year and lower concentrations during the monsoon period.

### Machine-Learning Performance

| Model | MAE (µg/m³) | RMSE (µg/m³) | R² |
|---|---:|---:|---:|
| Random Forest | 3.032 | 4.878 | 0.963 |
| Linear Regression | 3.122 | 5.057 | 0.961 |
| Persistence Baseline | 4.844 | 7.001 | 0.924 |

Random Forest achieved the lowest prediction errors on the held-out test period.

The current PM2.5 concentration was the most influential feature in the Random Forest model.

## Technologies Used

Python, Google Colab, Pandas, NumPy, Matplotlib,
