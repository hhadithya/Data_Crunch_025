# Harveston Climate Forecasting

## Overview
**Harveston Climate Forecasting** is a project aimed at developing accurate time series forecasting models for key environmental variables affecting agricultural productivity. By leveraging advanced machine learning techniques, this project enables informed decision-making for farmers in Harveston.

## Project Details
### Forecasting Objectives
The goal of this project is to predict five critical environmental variables:
- **Average Temperature (°C)**
- **Radiation (W/m²)**
- **Rain Amount (mm)**
- **Wind Speed (km/h)**
- **Wind Direction (°)**

These predictions assist in optimizing planting cycles, resource allocation, and preparing for weather extremes.

### Data Analysis & Key Findings
- **Temporal Patterns**: Seasonal trends were observed in temperature, radiation, and rain amount.
- **Geographic Variations**: Climate patterns varied across kingdoms based on latitude and longitude.
- **Data Inconsistencies**: Temperature values were recorded in both Celsius and Kelvin, requiring standardization.
- **Cyclic Patterns**: Wind direction displayed circular behavior, necessitating special handling.
- **Correlations**:
  - High correlation between **radiation and evapotranspiration (0.95)**.
  - Strong relationship between **feels-like temperature and average temperature (0.91)**.
  - Negative correlation between **rain duration and evapotranspiration (-0.71)**.

### Data Preprocessing
- **Unit Standardization**: Converted Kelvin to Celsius.
- **Outlier Handling**: Used **Winsorization** to cap extreme values.
- **Date Formatting**: Adjusted relative years to avoid invalid dates.
- **Time Series Preparation**: Structured data for LSTM models.

## Feature Engineering
To enhance model performance, various features were created:
- **Temporal Features**: Extracted seasonal elements and applied cyclical encoding.
- **Lagged Features**: Incorporated past values (1, 3, 7, 14, 30 days) to capture trends.
- **Moving Averages**: Calculated rolling means (7-day, 14-day, 30-day).
- **Geographic Grouping**: Merged kingdoms with similar locations to reduce redundancy.
- **Feature Selection**:
  - Used **Lasso regression** and **tree-based models** to retain relevant features.
  - Removed highly correlated (>0.95) and low-variance features.

## Model Selection
Several models were evaluated:
- **Random Forest Regressor**: Effective but lacked long-term forecasting ability.
- **ARIMA**: Limited due to multi-feature dependencies.
- **LSTM**: Performed inconsistently across variables.
- **CNN**: Outperformed LSTM with **>70% accuracy**.
- **Hybrid LSTM + CNN**: Less effective than standalone CNN.

### Final Model Choice
**CNN was selected** due to:
- High accuracy and generalizability.
- Effective handling of complex temporal dependencies.
- Computational efficiency and scalability.

## Model Evaluation
### Metrics Used
- **Root Mean Square Error (RMSE)** – for primary evaluation.
- **Mean Absolute Error (MAE)** – for measuring forecast error magnitude.

### Performance Insights
- **CNN model** achieved the best results across forecasting targets.
- Accuracy decreased for **long-term forecasts (>14 days)**.
- Extreme weather events were harder to predict.

## Real-World Applications
The forecasting models developed can be applied in:
- **Crop Selection Optimization**: Guiding farmers in selecting suitable crop varieties.
- **Resource Allocation Planning**: Optimizing irrigation and workforce management.
- **Risk Management**: Early warning systems for extreme weather conditions.
- **Yield Prediction**: Climate forecasts integrated with crop yield models.
- **Adaptive Farming**: Long-term infrastructure investments based on climate trends.

## Future Improvements
- Implement specialized models for extreme weather prediction.
- Improve long-term forecast accuracy using hierarchical models.
- Enhance efficiency with automated feature selection.
- Develop a user-friendly dashboard for real-time forecast visualization.

## Contributors
**Team:** RainMakers - Data_Crunch_025  
**Institution:** University of Moratuwa

## Team Members
- [B.A.Akith Chandinu](https://github.com/Akith-002)
- [Harindu Hadithya](https://github.com/hhadithya)
- [Vinuka Vilhan Fernandopulle](https://github.com/VinukaVilhan)

## License
This project is open-source and available for further improvements and contributions.
