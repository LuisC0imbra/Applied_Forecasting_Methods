# Applied Forecasting Methods - Time Series Analysis and Forecasting

**Python | Pandas | NumPy | Statsmodels | StatsForecast | Matplotlib | Plotly | Time Series Analysis**

## Project Overview

This project was developed during my Master's Degree in **Data Analysis and Decision Support Systems**, as part of the **Applied Forecasting Methods (Métodos de Previsão Aplicados)** course at ISCAC, during the 2022/2023 academic year.

**Final Grade: 16/20**

The project consists of three Jupyter notebooks, each covering a different stage of time series analysis and forecasting.

I worked with bicycle traffic data from German cities, starting with data preparation and exploratory analysis, moving on to time series decomposition, and finally comparing forecasting models to predict future bicycle traffic.

**Language note:** The three notebooks are written in Portuguese because they were originally submitted as coursework. They include the original assignment questions, Python code, explanations, and results. This README provides an overview in English.

## Dataset

**Source:** [Bicycle Data - Open Bicycle Data](https://www.bicycle-data.de/bicycles-data/)

The datasets contain bicycle counts recorded at monitoring stations in Germany.

Two locations were used:

- Berlin - Station 27-RE-MAR, with observations from January 2017 to June 2020.
- Munich - Kreuther station, used for the second and third parts of the project.

The data includes timestamps and bicycle counts, allowing the analysis of daily, weekly, and monthly patterns.

## Project Structure

The assignment was divided into three parts:

| Notebook | Main Focus | Assignment Weight |
|---|---|---|
| [Part 1](MPA_PART1.ipynb) | Data preparation and exploratory time series analysis | 25% |
| [Part 2](MPA_PART2.ipynb) | Missing data, seasonality, decomposition, and outliers | 40% |
| [Part 3](MPA_PART3.ipynb) | Forecasting models, cross-validation, and evaluation | 35% |

## 1. Part 1 - Data Preparation and Exploratory Analysis

In the first notebook, I worked with bicycle traffic data from Berlin.

The main objective was to prepare the time series and understand its structure before moving on to more advanced analysis.

### Data Preparation

I started by importing the CSV dataset using Pandas and inspecting the columns, data types, and observations.

I then converted the date columns into the correct datetime format and used timestamps as the basis for the time series.

### Timestamp Validation

I checked whether the observations followed the expected 15-minute frequency, including the changes between summer and winter time.

I also investigated missing timestamps and used Pandas to create a regular time index, leaving missing observations as NaN where appropriate.

### Exploratory Analysis

Finally, I aggregated bicycle counts at different frequencies:

- Daily bicycle traffic
- Weekly bicycle traffic
- Monthly bicycle traffic

The visualizations suggested that bicycle activity was generally higher during warmer periods.

This first part helped establish the importance of data quality and correct timestamp handling in time series analysis.

## 2. Part 2 - Time Series Analysis and Decomposition

The second notebook focused on bicycle traffic recorded at the Kreuther station in Munich.

This part involved a more detailed analysis of the time series, including missing data treatment, seasonality, trend identification, and outlier detection.

### Missing Data

I inspected the missing observations and explored different approaches to filling gaps in the dataset.

The goal was to prepare a more complete time series for the following analysis.

### Time Series Components

I converted the bicycle counts into a daily series and explored the main components:

- Trend - Long-term changes in bicycle traffic
- Seasonality - Recurring patterns over time
- Residuals - Variation not explained by the trend and seasonal components

I used time series plots and autocorrelation analysis to better understand the behavior of the data.

### Time Series Decomposition

I applied and compared several decomposition approaches:

- Classical additive decomposition
- Classical multiplicative decomposition
- STL decomposition

These methods helped separate the underlying trend, seasonal patterns, and residual variation.

### Outlier Detection

I also explored unusual observations using the results of the time series decomposition.

### Additional Analysis

The final section investigated two questions:

- Did the COVID-19 pandemic affect bicycle traffic patterns?
- Is bicycle usage higher during milder weather conditions?

These analyses connected the statistical results with possible real-world explanations for changes in bicycle activity.

## 3. Part 3 - Forecasting and Model Evaluation

The third notebook focused on forecasting future bicycle traffic using the Munich dataset.

I compared different statistical forecasting methods and evaluated their performance before selecting a model.

### Forecasting Models

I used the Python StatsForecast library to test several approaches:

- Seasonal Naive
- Automatic ARIMA
- ARIMA with first-order differencing
- Automatic ETS
- ETS with a damped trend configuration

The objective was to compare simpler forecasting methods with more advanced statistical models.

### Forecasting the Next 14 Days

The first forecasting task involved predicting daily bicycle counts for a 14-day period, from December 1 to December 14, 2021.

I generated forecasts and used time series cross-validation to evaluate the models.

### Model Evaluation

I compared the forecasting errors using three metrics:

| Metric | Description |
|---|---|
| MAE | Mean Absolute Error |
| RMSE | Root Mean Squared Error |
| MAPE | Mean Absolute Percentage Error |

Based on the error comparison recorded in the notebook, the ARIMA model with first-order differencing was selected.

I then generated the final forecasts, examined prediction intervals, and analyzed the model residuals using visualizations and autocorrelation.

### One-Day-Ahead Forecasting

The second forecasting task focused on predicting bicycle traffic for December 1, 2021.

I repeated the model comparison using a one-day forecast horizon and time series cross-validation.

The ARIMA model with first-order differencing was again selected based on the results documented in the notebook.

This part gave me practical experience with forecasting horizons, model selection, error metrics, and the importance of evaluating predictions on time-ordered data.

## 4. Key Learnings

Working through these three assignments helped me develop several skills:

- Preparing and validating timestamp-based datasets
- Identifying missing observations in time series
- Resampling data into different time frequencies
- Understanding trends and seasonal patterns
- Applying classical and STL decomposition
- Identifying unusual observations and possible outliers
- Comparing statistical forecasting models
- Evaluating forecasts with cross-validation and error metrics
- Interpreting prediction intervals and residual diagnostics

The project also showed me how data preparation, exploratory analysis, and model evaluation are connected in a complete forecasting workflow.

## 5. Technologies Used

| Technology | Purpose |
|---|---|
| Python | Data analysis and forecasting |
| Pandas | Data preparation and time series manipulation |
| NumPy | Numerical calculations |
| Statsmodels | Time series analysis and decomposition |
| StatsForecast | Statistical forecasting models |
| Matplotlib | Data visualization |
| Seaborn | Exploratory visualization |
| Plotly | Interactive visualizations |
| Google Colab / Jupyter Notebook | Development environment |

## 6. Repository Files

```text
Applied_Forecasting_Methods/
├── README.md
├── MPA_PART1.ipynb
├── MPA_PART2.ipynb
└── MPA_PART3.ipynb
```

The notebooks contain the original academic work in Portuguese, including the assignment questions and solutions.

Some cells use the original CSV paths from Google Colab or Google Drive, so these paths may need to be updated before running the notebooks in a different environment.

## 7. Academic Context

**Degree:** Master's Degree in Data Analysis and Decision Support Systems

**Institution:** ISCAC - Coimbra Business School

**Course:** Applied Forecasting Methods (Métodos de Previsão Aplicados)

**Academic Year:** 2022/2023

**Final Grade:** 16/20

This project was completed as part of the course assessment and represents my academic work in time series analysis and statistical forecasting.

Parts 2 and 3 were completed in collaboration with a fellow student, as indicated in the original notebooks.

---
