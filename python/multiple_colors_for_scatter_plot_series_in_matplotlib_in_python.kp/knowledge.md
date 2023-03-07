---
title: Changing the color of individual series in a scatter plot using matplotlib
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `c` parameter with a different list of colors for each series in the scatter function on matplotlib in Python.
---

**Contents**

[TOC]

Section 1: Introduction
Matplotlib is a popular data visualization library in Python. One of the most popular types of plots is the scatter plot, which is used to visualize the relationship between two numerical variables. In a scatter plot, different series are usually represented by different colors. In this tutorial, we will explore different ways to set different colors for each series in a scatter plot on Matplotlib in Python.

Section 2: Generating Data
Before we can create a scatter plot, we need to generate some data. We can use the NumPy library to generate random data. In the following code, we will generate two arrays, x and y, with 50 random numbers between 0 and 1.

```python
import numpy as np

# generate data
np.random.seed(42)
x = np.random.rand(50)
y = np.random.rand(50)
```

Section 3: Creating a Scatter Plot with Different Colors for Each Series
There are different ways to set different colors for each series in a scatter plot on Matplotlib. One way is to create a loop that iterates over the different colors and the data arrays. In the following code, we will use a for loop to plot the data points with different colors.

```python
import matplotlib.pyplot as plt

# create a scatter plot with different colors for each series
colors = ["r", "b", "g", "y", "m"]
for i in range(len(x)):
    plt.scatter(x[i], y[i], color=colors[i%5])

plt.show()
```

In the above code, we first defined a list of colors. We then used a for loop to plot each data point with a different color. We used the modulo operator to cycle through the colors list if the number of data points was greater than the number of colors.

Section 4: Conclusion
In this tutorial, we explored different ways to set different colors for each series in a scatter plot on Matplotlib in Python. We generated some random data using the NumPy library and created a scatter plot with different colors for each series using a for loop. There are other ways to set different colors for each series, such as using the c parameter to map a color value to the data values or using a colormap to map a color range to the data values. These methods are useful for more complex data sets with a larger number of data points.
