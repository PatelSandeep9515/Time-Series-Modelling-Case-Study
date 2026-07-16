# Time Series Modelling Case Study

## Forecasting German Electricity Demand Using Statistical, Machine Learning and Deep Learning Models

---

## Student Information

**Student Name:** Sandeep Patel

**Student ID:** 24077052

**Course:** MSc Data Science

**University:** University of Hertfordshire

**Module:** Time Series Analysis

**Assignment:** Time Series Modelling Case Study (40%)

**Submission Date:** 16 July 2026

---

## Project Overview

This project investigates German electricity demand forecasting using statistical, machine learning and deep learning techniques. The objective is to compare the forecasting performance of benchmark models, SARIMA, SARIMAX, Random Forest, Gradient Boosting and Long Short-Term Memory (LSTM) using historical electricity demand data.

The project follows a complete forecasting pipeline including data preprocessing, exploratory data analysis, stationarity testing, statistical modelling, feature-based machine learning, deep learning, model evaluation and comparative analysis.

---

## Objectives

- Perform exploratory analysis of German electricity demand.
- Test stationarity using ADF, ACF and PACF.
- Develop benchmark forecasting models.
- Implement SARIMA and SARIMAX models.
- Develop Random Forest and Gradient Boosting regression models.
- Build and train an LSTM network using hourly electricity demand.
- Compare forecasting performance using multiple evaluation metrics.
- Recommend the most suitable forecasting model for operational use.

---

## Dataset

### Electricity Demand

Open Power System Data (Germany)

https://data.open-power-system-data.org/time_series/

Period Used:

- January 2015 – October 2020

Original Resolution:

- Hourly

Model Data

- Weekly (Benchmark, SARIMA, SARIMAX, Random Forest, Gradient Boosting)
- Hourly (LSTM)

---

### Temperature Data

Berlin Historical Weather Data

Open-Meteo Archive API

https://archive-api.open-meteo.com/

Temperature was incorporated as an exogenous variable for the SARIMAX and feature-based regression models.

---

## Repository Structure

```
Time-Series-Modelling-Case-Study/

│
├── README.md
├── requirements.txt
├── LICENSE
├── .gitignore
│
├── notebook/
│   └── Time_Series_Modelling_Case_Study.ipynb
│
├── figures/
│   ├── weekly_electricity_load.png
│   ├── acf_plot.png
│   ├── pacf_plot.png
│   ├── sarima_forecast.png
│   ├── sarimax_forecast.png
│   ├── random_forest_forecast.png
│   ├── lstm_forecast.png
│   ├── comparison_forecasts.png
│   └── lstm_learning_curve.png
│
├── report/
│   └── Time_Series_Report.pdf
│
└── data/
```

---

## Models Implemented

### Benchmark Models

- Mean Forecast
- Naïve Forecast
- Seasonal Naïve
- Drift Forecast

### Statistical Models

- SARIMA
- SARIMAX

### Machine Learning Models

- Random Forest Regressor
- Gradient Boosting Regressor

### Deep Learning

- Long Short-Term Memory (LSTM)

---

## Exploratory Data Analysis

The following analyses were performed before model development:

- Missing value analysis
- Weekly aggregation
- Time series visualization
- Seasonal pattern analysis
- Stationarity testing
- Augmented Dickey-Fuller (ADF) Test
- Autocorrelation Function (ACF)
- Partial Autocorrelation Function (PACF)

---

## Forecast Evaluation Metrics

The forecasting models were evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Square Error (RMSE)
- Mean Absolute Percentage Error (MAPE)
- Coefficient of Determination (R²)

---

## Model Performance

| Model | MAE | RMSE | MAPE | R² |
|------|------:|------:|------:|------:|
| Mean | 3788.83 | 4397.30 | 0.0697 | -0.0121 |
| Naïve | 3783.20 | 4459.11 | 0.0679 | -0.0408 |
| Seasonal Naïve | 2318.52 | 3006.76 | 0.0441 | 0.5268 |
| Drift | 4339.89 | 5117.96 | 0.0805 | -0.3710 |
| SARIMA | 8077.82 | 9434.25 | 0.1519 | -3.6588 |
| SARIMAX | 6738.31 | 7825.29 | 0.1268 | -2.2052 |
| Random Forest | 1619.51 | 2258.79 | 0.0310 | 0.7329 |
| Gradient Boosting | 1600.58 | 2200.89 | 0.0306 | 0.7465 |
| **LSTM** | **731.57** | **960.69** | **0.0135** | **0.9907** |

---

## Key Findings

- Seasonal Naïve provided the strongest benchmark performance.
- SARIMA successfully modelled seasonality but struggled with nonlinear demand patterns.
- SARIMAX improved upon SARIMA by incorporating temperature as an exogenous variable.
- Random Forest and Gradient Boosting substantially reduced forecasting errors.
- LSTM achieved the highest forecasting accuracy, producing the lowest RMSE (960.69) and highest R² (0.9907).

---

## Software and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Statsmodels
- Scikit-learn
- TensorFlow / Keras
- SciPy

---

## Installation

Install the required packages:

```bash
pip install -r requirements.txt
```

---

## Running the Project

1. Download the Open Power System Data dataset.
2. Download Berlin temperature data from Open-Meteo.
3. Open the notebook:

```
Time_Series_Modelling_Case_Study.ipynb
```

4. Run all notebook cells sequentially.
5. All figures, evaluation metrics and forecasts will be generated automatically.

---

## References

1. Hyndman, R.J. and Athanasopoulos, G. (2021). *Forecasting: Principles and Practice*. https://otexts.com/fpp3/

2. Box, G.E.P., Jenkins, G.M., Reinsel, G.C. and Ljung, G.M. (2015). *Time Series Analysis: Forecasting and Control*. https://www.wiley.com/en-us/Time+Series+Analysis:+Forecasting+and+Control,+5th+Edition-p-9781118675021

3. Hochreiter, S. and Schmidhuber, J. (1997). Long Short-Term Memory. https://doi.org/10.1162/neco.1997.9.8.1735

4. Breiman, L. (2001). Random Forests. https://doi.org/10.1023/A:1010933404324

5. Friedman, J.H. (2001). Gradient Boosting Machine. https://doi.org/10.1214/aos/1013203451

6. Open Power System Data. https://data.open-power-system-data.org/time_series/

7. Open-Meteo Historical Weather API. https://archive-api.open-meteo.com/

8. Pedregosa, F. et al. (2011). Scikit-learn: Machine Learning in Python. https://jmlr.org/papers/v12/pedregosa11a.html

---

## Author

**Sandeep Patel**

MSc Data Science

University of Hertfordshire

2026
