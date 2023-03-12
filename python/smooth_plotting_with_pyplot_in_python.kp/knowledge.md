---
title: Create a smooth line using pyplot
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To plot a smooth line with PyPlot in Python, use the plot function with the desired x and y values and then add the keyword argument `smooth` set to a value greater than 0.
---

**Contents**

[TOC]

## Importing necessary libraries
```python
import matplotlib.pyplot as plt
import numpy as np
```

## Generating data
We will generate some data to plot a smooth line using numpy's `linspace` function.

```python
x = np.linspace(0, 10, 100) # We want to plot a line from 0 to 10 with 100 data points
y = np.sin(x) # We will use sine function to generate y-values for each x-value
```

## Plotting the smooth line
We can now use matplotlib.pyplot's `plot` function to plot the smooth line. We will also add labels for x and y axis, as well as a title for the plot.

```python
plt.plot(x, y)
plt.xlabel("x-axis")
plt.ylabel("y-axis")
plt.title("Smooth line plot")
plt.show() # This will show the plot
```

Our smooth line plot with x-axis, y-axis labels and a title will now be displayed.
