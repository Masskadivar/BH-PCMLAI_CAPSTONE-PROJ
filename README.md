# BH-PCMLAI_CAPSTONE-PROJ
The repository contains my capstone project. (Hourly Energy Consumption)

We will be utilizing hourly power consumption data from PJM to perform our analysis. Specifically, we will focus on the PJM East region, which provides data spanning from 2002 to 2018. PJM (Pennsylvania, Jersey, Maryland) is a regional transmission organization (RTO) in the United States that operates the power grid and manages the wholesale electricity market for a large portion of the Eastern Interconnection. This dataset offers a comprehensive view of power consumption patterns over a significant time period in the eastern region. By leveraging this data, we can gain insights into energy usage trends and make informed decisions related to power management and optimization.

## Time Series Modeling
To predict future energy consumption, we can utilize time series modeling techniques. Here, we'll use three different approaches: 

1. ARIMA Model:
ARIMA (AutoRegressive Integrated Moving Average) is a popular time series forecasting model that captures the autocorrelation and trend in the data. 
2. XGBoost Model:
XGBoost (Extreme Gradient Boosting) is a powerful machine learning algorithm used for regression and classification tasks. It can also be applied to time series forecasting.
3. Prophet Model:
Prophet is a time series forecasting model developed by Facebook. It is designed to capture various time series components such as trend, seasonality, and holidays. 

## Results
Based on the results, here is the summary of the models and their corresponding RMSE scores:


Models------------------------------------	RMSE Score

AR(1)--------------------------------------	1842.51

ARIMA(0, 1, 0)-----------------------------	1866.22

ARIMA(0, 0, 1)-----------------------------	5156.50

ARIMA(1, 1, 1)------------------------------	545.62

ARIMA(2, 1, 2)-----------------------------	473.62

XGBoost-----------------------------------	3726.32

Prophet------------------------------------	4119.08


1. ARIMA Models:
    * The ARIMA(2, 1, 2) model performed the best among the tested ARIMA models, with an RMSE score of 473.62. 
    * It is important to select appropriate ARIMA parameters based on the data characteristics. In this case, AR(1) and ARIMA(0, 1, 0) also showed reasonably good performance.
2. XGBoost Model:
    * The XGBoost model achieved an RMSE score of 3726.32. This model utilizes a gradient boosting algorithm and is known for its ability to handle complex patterns and nonlinear relationships in the data.
3. Prophet Model:
    * The Prophet model achieved an RMSE score of 4119.08. 
    * Prophet is designed to be user-friendly and requires minimal parameter tuning.

In summary, the ARIMA(2, 1, 2) model achieved the lowest RMSE score, indicating the best predictive accuracy among the models considered. However, the XGBoost and Prophet models also performed reasonably well in predicting power consumption.

## Findings
1. Seasonal patterns: Energy consumption varies across seasons, with higher demand in summer for cooling and winter for heating.
2. Peak demand: Businesses should identify peak demand periods in each season and implement strategies to manage and reduce peak loads.
3. Seasonal efficiency initiatives: Tailored energy efficiency initiatives can be implemented in different seasons, such as optimizing cooling systems in summer and heating systems in winter.
4. Renewable energy utilization: Seasons with abundant sunlight or strong winds provide favorable conditions for harnessing renewable energy sources such as solar and wind power. Businesses can capitalize on these seasonal variations by integrating renewable energy technologies into their energy mix. This can help reduce reliance on traditional energy sources, decrease carbon emissions, and potentially generate cost savings.
5. Seasonal energy forecasting: Accurate forecasting of seasonal energy demand using advanced models enables proactive decision-making, resource planning, and budgeting.
These findings emphasize the importance of understanding seasonal variations in energy consumption and implementing targeted strategies to optimize energy management throughout the year.

## Suggestions for next steps
1. Outlier detection and handling: Implement outlier detection techniques to identify and handle any outliers in the data. 
2. Feature engineering: Explore additional features that might have an impact on energy consumption, such as weather data (temperature, humidity, etc.), holidays, or special events. 
3. Hyperparameter tuning: Optimize the hyperparameters of the ARIMA, XGBoost, and Prophet models. Use techniques like grid search or random search to find the best combination of hyperparameters that yields the lowest error.
4. Model ensemble: Consider creating an ensemble model by combining the predictions from multiple models. 
