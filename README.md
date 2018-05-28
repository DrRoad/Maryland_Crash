# Maryland_Crash
Maryland Crash Analysis - Predicting the probability of accidents on a given segment on a given time. This prediction can be used as an input to get safest route and to optimize ambulance car allocation.
# Data Cleaning and Aggregation files
- MRCA_Data_Aggregation.Rmd
- MRCA_Data_Cleaning_Formatting.Rmd
# Data pre-processing and modelling files
- MRCA_ML.ipynb

# Overview

- Merging eight different files which includes Road condition data, Weather Data, Person's data, Road map data, etc related to crash in Maryland.
- Performing preliminary analysis on the data set to completely understand the data, form some hypothesis, spot outliers and derive some new attributes. Also, performing Hot-Spot analysis using ArcGIS pro.

# Data Processing:
- Performing data cleaning to get a complete data frame with no NA's, missing values and remove outliers. 
- Performing data aggregation so as to avoid redundancy in data, to get the frequency of accidents per segments and to avoid high dimensional data in pre-processing stage.
- Performing Label Encoding, One Hot Encoding (dummy variables by avoiding dummy variable trap) and Feature Scaling on the data frame.

# Negative Sampling:
- Here, we have all the positive records (accident occurred) but not a single record when the accidents did not occurred.
- Any record for a particular time when there is "No Accident" in a particular segment can be considered to be a potential Negative Sample.

# Machine Learning and Deep Learning Model:
# Part #1: 
- To identify the risk level of a road segment when compared to other segments, we try to forecast #accidents per segment (only positive samples)
- We build a deep neural network to forecast #accidents on different segments and visualize it on map of Maryland.
# Part #2:
- Here, model finds the likelihood of an accident to occur on different segments (using negative and positive samples).
- Comparing results from Naive Bayes, SVM, Random Forest, Deep Neural Network.
# Part #3:
- Classifying accidents to identify the its severity by applying different ML algorithms.
# Part #4:
Research: Predicting next accident location based on temporal and spatial features using Recurrent Neural Network with Long Short Term Memory (RNN - LSTM).
