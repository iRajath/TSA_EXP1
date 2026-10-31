# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 31.10.2026

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.

# SOFTWARE USED:
Google Colab

# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:

```python

import matplotlib.pyplot as plt
import pandas as pd

df = pd.read_csv("Netflix-Subscriptions.csv")

df.head()

df['Time Period'] = pd.to_datetime(df['Time Period'])

df.dtypes

df.set_index('Time Period', inplace=True)

df_resampled = df['Subscribers'].resample('D').interpolate()

df_resampled.plot(kind='line', label='Total Subscribers', color='black')
plt.title('Time Series Plot of Netflix Subscribers')
plt.xlabel('Date')
plt.ylabel('Number of Subscribers')
plt.legend()
plt.grid(True)
plt.show()
```









# OUTPUT:

<img width="584" height="455" alt="image" src="https://github.com/user-attachments/assets/790fdf65-bf89-44d6-a8a3-ce563001d2ce" />





# RESULT:
Thus we have created the python code for plotting the time series of given data.
