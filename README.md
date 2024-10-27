# Time-Series-Analysis-for-Climate-Data
## Project Overview
This project covers statistical modeling and analysis for three climate-related datasets, focusing on precipitation in the Netherlands, global surface temperature anomalies, and UK daily temperatures. The report walks through various modeling techniques, including spatial and time series models, to understand and predict climatic variables.

## Contents
## 1. Precipitation Modeling in the Netherlands
In this section, I analyzed the monthly precipitation data for the Netherlands in September 2019. Key steps included spatial analysis using variogram and kriging models, as well as Gaussian Process and Bayesian methods.

### Data Visualization:
Plotted precipitation data across observation stations using a geospatial approach. By converting the data to a geodata object, I visualized spatial distributions and noted patterns and skewness.

### Modeling:
Sample Variogram and Kriging: Created a variogram to determine spatial correlation and modeled precipitation using kriging. The nugget was considered to account for spatial randomness, and assumptions regarding trend functions and covariance were clearly stated.
Gaussian Process Model: Applied a Gaussian Process model with maximum likelihood estimation to optimize parameters, fitting the data well under selected assumptions.
Bayesian Modeling: Built a Bayesian model with discrete priors based on estimates from the Gaussian Process model. Parameters were set with a discrete prior over the correlation length and nugget to improve accuracy.

### Prediction:
Predicted precipitation values at five selected test locations, comparing the performance of the kriging, Gaussian Process, and Bayesian models.

## 2. Global Surface Temperature Anomalies
In this part, I analyzed the global surface temperature anomaly dataset from 1850 to 2023, focusing on modeling post-1990 data and forecasting future temperature trends.

### Data Exploration:
Plotted global surface temperature anomalies to observe long-term trends and any significant changes.

### Model Fitting:
**ARMA/ARIMA Models:** Tested multiple ARMA and ARIMA models, ultimately selecting models based on goodness-of-fit criteria for monthly anomaly data.
**Quarterly Data Transformation:** Aggregated data into quarterly means, fitting ARMA and ARIMA models to capture broader temporal trends.
**Dynamic Linear Model:** Fitted a Dynamic Linear Model with linear trend and seasonal components, applied to both monthly and quarterly datasets.

### Forecasting:
Used the best-fitted models to forecast temperature anomalies for 2024, comparing the results across the different time series models for accuracy and consistency.

## 3. UK Daily Maximum Temperature in 2022
This section focused on spatial and time series analysis of maximum daily temperatures in the UK across 27 stations.

### Data Visualization:
Created spatial and temporal plots to examine daily temperature trends across the UK.

### Gaussian Process Model:
Fitted a spatial Gaussian Process model using maximum likelihood estimation to predict temperatures for specific locations (Wallington, Reading, and Whitby) on July 24th, 2022.
Produced visualizations of the mean and variance across a 0.05-degree grid to show predictive uncertainty across the region.

### Time Series Modeling:
Built time series models to forecast temperatures for Fair Isle (May 1-5) and Bridlington (October 31-November 4) without automated model selection. This involved manual testing of different configurations to ensure accurate predictions.
