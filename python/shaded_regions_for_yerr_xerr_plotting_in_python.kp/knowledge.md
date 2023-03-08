---
title: Instead of displaying error bars, represent the yerr/xerr as a shaded area in the graph
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the `fill\_between` function from Matplotlib to plot yerr/xerr as a shaded region.
---

**Contents**

[TOC]

Section 1: Introduction
When visualizing data with error bars in Python, it is common to use lines or bars to represent the mean values and error bars to represent the range of variation. However, there are cases where it might be more appropriate to use a shaded region instead of error bars, especially when dealing with highly variable data. In this tutorial, we will discuss how to plot yerr/xerr as a shaded region using Python's Matplotlib library.

Section 2: Generating data
Before we start plotting, let's generate some random data to work with. We will use NumPy to generate data with a mean of 0 and a standard deviation of 1. We will also create error values using NumPy's random module.

```python
import numpy as np

x = np.linspace(0, 10, 100)
y = np.sin(x)
y_err = np.random.uniform(0.1, 0.5, size=len(y))
```

Section 3: Plotting yerr as a shaded region
To plot yerr as a shaded region, we can use the fill_between function from Matplotlib. We will pass it the x values, the y values, and the upper and lower bounds of the shading, which are calculated by adding and subtracting the error values from the y values.

```python
import matplotlib.pyplot as plt

plt.plot(x, y)

plt.fill_between(x, y - y_err, y + y_err, alpha=0.3)
```

The alpha parameter controls the opacity of the shading. A value of 0 would make it completely transparent, while a value of 1 would make it completely opaque.

Section 4: Plotting xerr as a shaded region
To plot xerr as a shaded region, we can use the same fill_between function. We will need to transpose our data to make sure that the x values become the y values, and the y values become the x values.

```python
x_err = np.random.uniform(0.1, 0.5, size=len(x))

plt.plot(y, x)

plt.fill_betweenx(x, y - x_err, y + x_err, alpha=0.3)
```

Conclusion:
In this tutorial, we learned how to plot yerr/xerr as a shaded region in Python using Matplotlib's fill_between function. By creating shaded regions instead of error bars, we can better visualize highly variable data and highlight areas of uncertainty.
