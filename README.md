# Ex.No: 02 LINEAR AND POLYNOMIAL TREND ESTIMATION
Date:
### AIM:
To Implement Linear and Polynomial Trend Estiamtion Using Python.

### ALGORITHM:
Import necessary libraries (NumPy, Matplotlib)

Load the dataset

Calculate the linear trend values using least square method

Calculate the polynomial trend values using least square method

End the program
### PROGRAM:

```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

data=pd.read_csv("C:/Users/SEC/Downloads/archive/data_date.csv",parse_dates=['Date'],index_col='Date')

data.head()

resampled_data = data['AQI Value'].resample('Y').sum().to_frame()
resampled_data.head()

resampled_data.index = resampled_data.index.year

resampled_data.reset_index(inplace=True)
resampled_data.rename(columns={'Date': 'Year'}, inplace=True)

resampled_data.head()

years = resampled_data['Year'].tolist()
passengers = resampled_data['AQI Value'].tolist()

```

A - LINEAR TREND ESTIMATION

B- POLYNOMIAL TREND ESTIMATION

### OUTPUT
A - LINEAR TREND ESTIMATION

B- POLYNOMIAL TREND ESTIMATION

### RESULT:
Thus the python program for linear and Polynomial Trend Estiamtion has been executed successfully.
