# Transformers-for-Time-Series-Forecasting
Basic Transformer architecture is used to illustrate its capacity for time series forecasting and as a base for further enhancements.

I use the typical Energy Compsumption dataset from https://archive.ics.uci.edu/ml/datasets/Appliances+energy+prediction 

This datset has 10-min measurements of household appliances energy consumption (20 first features), coupled with local meteorological data (8 last features).
The time-series forecasting task is to predict the first 20 features, given as input data the 28 features. A window of observations of 12 time steps is considered to predict the next series of observations (this corresponds to a 2-hours window of observations.
The dataset variables names are:
dataset variables ['Appliances', 'lights', 'T1', 'RH_1', 'T2', 'RH_2', 'T3', 'RH_3', 'T4', 'RH_4', 'T5', 'RH_5', 'T6', 'RH_6', 'T7', 'RH_7', 'T8', 'RH_8', 'T9', 'RH_9', 'T_out', 'Press_mm_hg', 'RH_out', 'Windspeed', 'Visibility', 'Tdewpoint', 'rv1', 'rv2'].
The simple Transformer architecture in the code just uses the usual self-attention and position encodings. The training and validations errors are good as can be seen in the figure below.

![image alt](https://github.com/jhleonjg/Transformers-for-Time-Series-Forecasting/blob/main/TrainValErrors.png?raw=true)

The predictions are made for the next 12 datapoints. As can be seen in the plot below the forecasting is not so great this mainly because the amount of data is small. But this implementation serves its purpose to ilustrate the main building blocks of transformers in time series forecasting. I will test longer, more complex time series in the near future withe better feature engineering in it.

![image alt](https://github.com/jhleonjg/Transformers-for-Time-Series-Forecasting/blob/main/PredictionVsGroundTruth.png?raw=true)




