---
title: How to define the limits of x and y axes for a subplot
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To set xlim and ylim for a subplot in Python, use the set\_xlim() and set\_ylim() methods for the axes object of the subplot.
---

**Contents**

[TOC]

# Introduction
Sometimes it is necessary to set specific limits for the x and y axes in a subplot in Python. This can be done using the `set_xlim()` and `set_ylim()` methods for the subplot object.

# Getting Data
To demonstrate how to set the x and y axis limits for a subplot, we first need to generate some data to plot. This can be done by importing the numpy library and using the `linspace()` function to create an array of 100 x values ranging from 0 to 2π. We can then create a y array by taking the sine of the x values.

``` python
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(0, 2*np.pi, 100)
y = np.sin(x)
```

# Creating a Subplot
Next, we can create a figure with a single subplot using the `subplots()` function. We can then plot the x and y arrays on the subplot using the `plot()` method.

``` python
fig, ax = plt.subplots()
ax.plot(x, y)
```

# Setting Axis Limits
To set the axis limits for the subplot, we can use the `set_xlim()` and `set_ylim()` methods for the `ax` object. For example, to set the x axis limits to be between 0 and π, and the y axis limits to be between -1 and 1, we can use the following code:

``` python
ax.set_xlim([0, np.pi])
ax.set_ylim([-1, 1])
```

This will set the axis limits for the current subplot to the specified values. Note that we use square brackets `[]` around the limits to pass them as a list.

# Conclusion
In summary, setting the x and y axis limits for a subplot in Python can be done using the `set_xlim()` and `set_ylim()` methods for the subplot object. We first generated some data to plot, created a subplot, and then set the axis limits using the `set_xlim()` and `set_ylim()` methods.
