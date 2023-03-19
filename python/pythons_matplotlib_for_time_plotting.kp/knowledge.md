---
title: Using matplotlib to create time plots in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To plot time in Python with Matplotlib, you can use the matplotlib.dates module to convert the time data into a format that can be plotted on a graph.
---

**Contents**

[TOC]

## Introduction

Matplotlib is a data visualization library that is very useful for plotting time-series data. Time can be represented in various formats such as datetime objects, pandas Timestamps or simply as Unix timestamps. In this tutorial, we will explore how to plot time in Python with Matplotlib.

## Plotting time-series data with datetime objects

The first step is to create a datetime object. Datetime objects can be created using the datetime module in Python. Once we have our data in the datetime format, we can use Matplotlib to plot the data. Here is a sample code:


```python
import matplotlib.pyplot as plt
from datetime import datetime

# Sample data
x = [datetime(2021, 1, 1, 0, 0),
     datetime(2021, 1, 2, 0, 0),
     datetime(2021, 1, 3, 0, 0),
     datetime(2021, 1, 4, 0, 0)]

y = [4, 6, 2, 8]

# Plotting
plt.plot(x, y)
plt.show()
```

![image.png](attachment:image.png)

First, we import the necessary libraries. We create the datetime objects for the x-axis and a simple list for the y-axis. We then use the `plot()` function from Matplotlib to plot the data. Finally, we use `show()` to display the plot.

## Formatting dates on the X-axis

Matplotlib provides a lot of flexibility in formatting dates on the X-axis. We can use the `DateFormatter` class from the `matplotlib.dates` module to format the dates to our preference. Here's an example:

```python
import matplotlib.pyplot as plt
from datetime import datetime
import matplotlib.dates as mdates

# Sample data
x = [datetime(2021, 1, 1, 0, 0),
     datetime(2021, 1, 2, 0, 0),
     datetime(2021, 1, 3, 0, 0),
     datetime(2021, 1, 4, 0, 0)]

y = [4, 6, 2, 8]

# Plotting
fig, ax = plt.subplots()
ax.plot(x, y)

# Formatting the dates
date_fmt = '%d-%m-%Y' # Format the date as DD-MM-YYYY
date_formatter = mdates.DateFormatter(date_fmt)
ax.xaxis.set_major_formatter(date_formatter)
plt.show()
```

![image-2.png](attachment:image-2.png)

In this example, we set the `major_formatter` property of the x-axis to a `DateFormatter` object that formats the date in the format `DD-MM-YYYY`.

## Plotting time-series data with pandas Timestamps

Pandas is a very powerful data manipulation library that provides easy-to-use datetime indexing and formatting functionality. We can use pandas to read data from various formats such as CSV or Excel files, and then plot the data using Matplotlib. Here's an example:

```python
import pandas as pd
import matplotlib.pyplot as plt

# Read data from CSV file
data = pd.read_csv('data.csv')
data['Date'] = pd.to_datetime(data['Date']) # Convert the Date column to datetime format

# Plotting
fig, ax = plt.subplots()
ax.plot(data['Date'], data['Sales'])

# Formatting the dates
date_fmt = '%d-%m-%Y' # Format the date as DD-MM-YYYY
date_formatter = mdates.DateFormatter(date_fmt)
ax.xaxis.set_major_formatter(date_formatter)

plt.show()
```

In this example, we read data from a CSV file, convert the `Date` column to a datetime object using the `to_datetime()` function, and then plot the data using Matplotlib. We also format the dates on the X-axis using the `DateFormatter` class.

## Conclusion

In this tutorial, we learned how to plot time in Python using Matplotlib. We explored different methods such as using the datetime module, formatting dates on the X-axis, and plotting time-series data using pandas Timestamps. With these tools in our arsenal, we can effectively plot and visualize time-series data for various applications.
