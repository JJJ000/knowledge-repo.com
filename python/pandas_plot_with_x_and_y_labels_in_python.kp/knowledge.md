---
title: Add labels for the x-axis and y-axis on a plot created with pandas
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To add x and y labels to a pandas plot in Python, use the `set\_xlabel()` and `set\_ylabel()` methods.
---

**Contents**

[TOC]

## Importing necessary libraries
Before plotting, we need to import pandas and matplotlib libraries. To do that, we can use the code below:
```python
import pandas as pd
import matplotlib.pyplot as plt
```

## Reading the data
We can use the Pandas `read_csv()` function to read a CSV file and store the data in a dataframe object. In this example, let's assume that we have a CSV file named `data.csv` that contains two columns of data, `x_values` and `y_values`. We can read that file and store the data in a dataframe object using the following code:
```python
data = pd.read_csv('data.csv')
```

## Plotting with x and y labels
After reading the data, we can create a scatter plot using the `plot()` function provided by Pandas. We can also add x and y axis labels to the plot using the `set_xlabel()` and `set_ylabel()` functions provided by Matplotlib, as shown in the code below:
```python
data.plot(kind='scatter', x='x_values', y='y_values')
plt.xlabel('X Axis Label')
plt.ylabel('Y Axis Label')
plt.show()
```

The above code creates a scatter plot with x and y axis labels. Change the x and y values and labels according to the data and desired labels.
