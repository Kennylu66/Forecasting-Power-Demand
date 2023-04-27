# Forecasting Power Demand
For this project, we will be using the Electricity Transformer Dataset (ETDataset). It contains hourly data collected from 2 electricity transformers at 2 stations from two different regions of the same province in China in 2 years (17420 data points). Each data point contains 8-dimensional features, including the record date and time of the data point, the predicted value "oil temperature (OT)", and 6 different types of external load values, "HUFL", "HULL", "MUFL", "MULL", "LUFL", "LULL".

The project aims to implement and compare a variety of Machine Learning models, including traditional ML algorithms such as Support Vector Regression (SVR), Random Forest Regression (RF), K-Nearest Neighbour Regression (KNN), and Deep Learning models such as Gated Recurrent Unit (GRU) and Recurrent Neural Network (RNN), based on the datasets of 6-dimensional features to predict the target, oil temperature.

We use Root Mean Square Error (RMSE), Mean Squared Error (MSE), Mean Absolute Error (MAE) and coefficient of determination (R2) as our main evaluation function. They provide comprehensive measures of errors. Our forecasting tasks are defined on various time scales. The shorter ones are using the past OT values and current features to forecast the next 1h (corresponding to 1 data point), next 2h, next 4h OT values. The long-term forecasts are 12h, 24h and 48h. As the time goes longer, the error gets accumulated and increases non-linearly. While most of our models perform well on the one-step forecasting (next 1h), the longer term forecast shows the difference of different methods. In the traditional machine learning methods, the SVM (support vector machine) outperforms RF(random forest) and KNN(k nearest neighbors). More complex neural networks doesn’t necessarily performs better for our relatively small dataset.
