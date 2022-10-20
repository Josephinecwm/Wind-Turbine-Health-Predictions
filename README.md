# Deep Learning - Wind Turbine Health Prediction
In modern industrial applications, sensors are used to observe key machine characteristics.
These can help detect slight deviations and issues to avoid major system failures through
targeted repairs while keeping maintenance costs under control. Such sensors are critical in the operation of wind turbines, and sensor readings need to be reliably converted into operating mode.

Given the sensor readings overtime, we are interested in knowing whether the turbine is operating correctly or whether one of several issues is present. This project aims to predict, as accurately as possible, the operating mode of a wind turbine based on the time series data from two sensors of a wind turbine. Deep learning models of LSTM, GRU, convolutional 1-D RNNs, 2D-CNN and CNN using a pretrained MobileNet architecture are built (Python - Tensorflow), compared and assesed to find the best model with minimised monetary cost.

## data information
The data are sensor readings and operating modes for 4,000 turbine runs. 
time_series_1 and time_series_2 are NumPy arrays of shape (4000,5000). 
Each observation corresponds to 5,000 records of the turbine over time by one of the two sensors (time_series_1 measures the pitch angle in each second of operation, and time_series_2 measures the generator torque). 
y is the operating mode for each of the 4,000 turbine runs: 
- 0 if the turbine is healthy
- 1 if the generator torque is faulty
- 2 if the pitch angle is faulty
- 3 if both are faulty

*Note: wind_turbine.ipynb contains the full script with detailed analysis of each model.
