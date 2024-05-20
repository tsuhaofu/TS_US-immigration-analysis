# US Immigration Analysis

This project analyzes the trends in annual immigration levels in the United States and forecasts future immigration numbers using time-series analysis techniques.

## Introduction
This analysis covers the period from 1820 to 1920, capturing the evolution of immigration trends due to changes in policy and global events. The study aims to model these trends accurately and forecast immigration levels for future years.

## Data
The current report utilized immigrant data published by the Department of Homeland Security (DHS). The dataset includes the total number of U.S. immigrants annually from 1820 to 1920. The data shows a generally increasing trend with peaks influenced by policy changes and global events such as World War I and the Great Depression.

## Exploratory Data Analysis (EDA)
- **Trend Analysis**: The data exhibits a clear deterministic trend, with immigration numbers peaking in the early 20th century and then declining due to restrictive laws and global conflicts.
- **Log Transformation**: Applied to stabilize variance and improve normality. The transformed data shows a persistent increasing trend, suggesting non-stationarity.

## Methodology
### Stationarity Testing
- **Augmented Dickey-Fuller Test**: After the first difference, the series becomes stationary, indicating no unit root and allowing for further analysis.
  
### Time Series Modeling
- **ARIMA Model**: After a grid search for optimal hyperparameters, the ARIMA(2, 1, 6) model was selected, effectively capturing autocorrelations and trends. Parameters were determined based on ACF and PACF analyses.

### Forcasting
The model was used to predict immigration levels from 1963 to 1970, including 80% and 95% confidence intervals. 
The forecasts suggest a gradual increase in immigration over the next eight years.

## Results
- **Model Fit**: The ARIMA (2, 1, 6) model provided a homoscedastic fit with residuals centered around zero mean, suggesting a good fit.
- **Ljung-Box Test**: Confirmed no significant autocorrelation in residuals, indicating the model captured all significant autocorrelations.
  
## Conclusion
The analysis successfully models and forecasts U.S. immigration trends using ARIMA techniques. The study provides insights into how historical events and policies have shaped immigration patterns and predicts future trends based on these models.


