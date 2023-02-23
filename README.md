# wind_power_predictions
This notebook is created to predict wind power predictions using the Wind Turbine Scada Dataset (https://www.kaggle.com/datasets/berkerisen/wind-turbine-scada-dataset). In Wind Turbines, Scada Systems measure and save data's like wind speed, wind direction, generated power etc. for 10 minutes intervals. This file was taken from a wind turbine's scada system that is working and generating power in Turkey.

The data includes:
- Date/Time (for 10 minutes intervals)
- LV ActivePower (kW): The power generated by the turbine for that moment
- Wind Speed (m/s): The wind speed at the hub height of the turbine (the wind speed that turbine use for electricity generation)
- Theoretical_Power_Curve (KWh): The theoretical power values that the turbine generates with that wind speed which is given by the turbine manufacturer
- Wind Direction (°): The wind direction at the hub height of the turbine (wind turbines turn to this direction automatically)

After analyzing the data, we found out that:
1. On average, 6:00 a.m. to 2:00 p.m. produces the least amount of energy in a 24-hour period
2. The 1st fact is due to the fact that it is at this time that the wind blows at a lower speed
3. The most energy is generated in March and November
4. However, the least amount of energy is produced in April, July, October and December
5. There is an understandable correlation that the lowest wind speeds are in the same months as in fact 4. 
6. The power production reaches near a maximum level after the wind speed reaches 15 m/s.
7. The south and southwest winds have the greatest speed
8. The south and southwest types of winds are not as common as the northeast wind, and the speed of the northeast wind is slightly less than the south winds. 
9. The wind turbine produces more power if the wind blows from the N-E and S-SW directions


In the project I used algorithms such as Decision Tree Regressor, Random Forest Regressor, Extra Trees Regressor, Ada Boost Regressor, Gradient Boosting Regressor, Extreme Gradient Boosting Regressor (XGBRegressor), LGBMRegressor.

At each model I measured 3 metrics: **R Squared Score (R2), Mean Absolute Error (MAE), Root Mean Squared Error (RMSE)**

According to the metrics, the best algorithms are **LGBMRegressor, Extra Trees Regressor, Random Forest Regressor**
