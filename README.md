# Appliances_Energy_prediction_ML_Model_Regression
Appliance energy prediction using linear regression models
Capstone-Project-On-Appliance_Energy_Prediction
**Introduction**

In today's world, the use of energy is quickly expanding. We are experiencing a lack of energy as a result of increased energy consumption in some regions of the world, which is causing environmental damage. We are dealing with excessive energy consumption in home appliances in some places, so our main goal in this project is to analyze what factors are influencing the increasing energy consumption of home appliances, how we can reduce energy consumption of home appliances, and predict energy consumption of appliances using regression models.
This project will analyze the Energy dataset using visualizations and graphs created with Python packages such as sklearn, matplotlib, Seaborn, and Eli5.

**Abstract**

Because of the transition towards the Internet of Everything, predicting the energy required by household appliances is a difficult study topic. The energy consumptions of appliances were forecasted in this work using an ML model-based strategy that employed the linear, lasso, ridge, decision tree, random forest, gradient boosting, xgb, adaboost, and lgbm regression algorithms. The current study has two goals: to maximize the prediction performance of the algorithms and to minimize the number of selected features. The proposed method was evaluated on an appliance energy prediction dataset taken from Reliable Prognosis' public dataset.

**Dataset information**

**Date time year- month-day hour:**minute:second

**Appliances- **energy use in Wh


**Lights- **energy use of light fixtures in the house in Wh

**T1- **Temperature in kitchen area, in Celsius

**RH_1- **Humidity in kitchen area, in %
**T2- **Temperature in living room area, in Celsius
**RH_2- **Humidity in living room area, in %
**T3- **Temperature in laundry room area
**RH_3- **Humidity in laundry room area, in %
**T4- **Temperature in office room, in Celsius
**RH_4- **Humidity in office room, in %
**T5- **Temperature in bathroom, in Celsius
**RH_5- **Humidity in bathroom, in %
**T6- **Temperature outside the building (north side), in Celsius
**RH_6- **Humidity outside the building (north side), in %
**T7- **Temperature in ironing room , in Celsius
**RH_7- **Humidity in ironing room, in %
**T8- **Temperature in teenager room 2, in Celsius
**RH_8- **Humidity in teenager room 2, in %
**T9- **Temperature in parents room, in Celsius
**RH_9- **Humidity in parents room, in %
**To- **Temperature outside (from Chievres weather station), in Celsius
**Pressure **(from Chievres weather station)- in mm Hg
**RH_out- **Humidity outside (from Chievres weather station), in %
**Wind speed **(from Chievres weather station)- in m/s
**Visibility **(from Chievres weather station)- in km
**Tdewpoint **(from Chievres weather station)- Â°C
**rv1- Random variable 1, nondimensional
rv2- Random variable 2, nondimensional**
Where indicated, hourly data (then interpolated) from the nearest airport weather station (Chievres Airport, Belgium) was downloaded from a public data set from Reliable Prognosis, rp5.ru. Permission was obtained from Reliable Prognosis for the distribution of the 4.5 months of weather data.

** Problem Statement**
For approximately 4.5 months, the data set is set to 10 minutes. A ZigBee wireless sensor network was used to monitor the house's temperature and humidity levels. Every wireless node reported the temperature and humidity levels every 3.3 minutes. The wireless data was then averaged over 10 minute periods. The energy data was recorded every 10 minutes using m-bus energy metres. Weather from the nearest airport weather station (Chievres Airport, Belgium) was collected from a public data set from Reliable Prognosis (rp5.ru) and blended with the experimental data sets using the date and time columns. Two random variables were included in the data set to test the regression models and to filter out non-predictive features (parameters).
The problem statement is to create a machine learning model that can accurately forecast energy usage based on the supplied features. This might be valuable for building managers, energy firms, and policymakers who need to optimize energy consumption, cut costs, and minimize the environmental impact of energy usage.
Specifically, the model should be able to reliably anticipate energy usage based on the different elements that influence energy consumption, such as temperature, humidity, illumination, and time of day. This can assist building managers and energy firms in identifying patterns and trends in energy consumption and making informed energy decisions, such as altering HVAC settings, optimizing lighting, or introducing energy-efficient solutions. Policymakers can also use this data to create regulations and incentives that encourage energy efficiency and sustainability.

** Approaches**

This study seeks to forecast the energy usage of household appliances. With the emergence of smart homes and the growing demand for energy management, existing smart home systems can benefit from accurate predictions. If the energy usage of appliances can be forecasted for every potential condition, then device control can be optimized for energy savings as well. This is an example of Regression analysis, which is part of the Supervised Learning problem. The goal variable is appliance energy usage, and the characteristics are sensor data and weather data.
We will get some insights from data visualisation after retrieving the information from the date column and analyzing it so that we can determine the aspects that will influence the output, such as energy consumption by appliances, which is a big issue and one of the most pressing concerns for the Green Economy.
For reproductive analysis, we will break this endeavor into five parts.
The first stage will be to analyze, clean up the dataset that was provided, and remove some extraneous columns.
In the next step we will draw some insights after fetching the other details from date column like hourly, daily and monthly energy consumption. After that we will do Feature selection and Engineering. In FE we will be using VIF and correlation both method for Removing Multicollinearity and drop Some unnecessary column.
Then we will split our data into train and test set after that we used some scaling techniques on train set and after that we prepare our data for feeding to our models for training and analyze the results of all models by comparing with each other. We will select best model among these and proceed with them further.
In the final phase, we will tune the hyperparameters of our topmost model to see how it responds to different parameters. After we have determined the best parameters for our top models, we will use the feature importance approach to calculate the weightage of all features for our top model using ELi5.

**Conclusion**

•	Linear Regression, Lasso Regression, Ridge Regression, Elasticnet Regressor, DecisionTree Regressor, are used to predict household appliance energy consumption.

•	We compare and evaluate the best model with the lowest error and the greatest R-squared score after suitable preprocessing and fitting the fourteen models.

•	T6 and T_out, T9 and T7 had a high association with each other, thus we deleted T6 and T9. When examining the influence of the Random Variable attribute, the linear models assigned the random variable near zero weights, negating its influence in predicting the target variable.

•	Inside room temperature and humidity has high variance inflation factor(VIF) so,we had to drop them

•	Light consumption was evaluated highly when all factors were used. When evaluating different predictor subgroups, eliminating light usage did not appear to have a substantial influence. This could indicate that other characteristics are well connected with light energy usage.

•	The pressure's significant prediction power could be attributed to its influence on wind speed and higher rainfall probability, which could potentially raise the occupancy of the residence.

•	Because this dataset involves a temporal component, we believe that employing temporal Series Analysis techniques will result in superior results.

•	ExtraTreeRegressor was discovered to be the best performing model, with an R-squared value of 0.7362

•	Appliances hu_build_out Windspeed Tdewpoint month weekday hour Humidity_difference all play a part in energy prediction.


