---
title: What is the method for drawing a grid on a plot in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the plt.grid() function from the matplotlib library in Python to draw a grid onto a plot.
---

**Contents**

[TOC]

## Import Libraries

The following libraries are used to draw a grid onto a plot. Import them using the following code:

```python
import matplotlib.pyplot as plt
import numpy as np
```


## Create Arrays

To create an array in NumPy, use the `numpy.array()` method. This method takes a list as an argument and converts it into an array. In this example, we will create an array of x values and y values. 

```python
x = np.arange(1, 11) # Array containing values from 1 to 10

y = x**2 # Array containing square of values from 1 to 10
```


## Plot the Data and Add Grid

The following code plots the data and adds a grid. The `plt.plot()` method is used to plot the x and y values. The `plt.grid()` method is used to add a grid.

```python
plt.plot(x, y)
plt.grid(True)
plt.show()
```


## Customizing the Grid

You can customize the grid by setting various parameters in the `plt.grid()` method. The following code shows an example of customizing the grid:

```python
plt.plot(x, y)
plt.grid(True, linestyle='--', linewidth=0.5, color='gray')
plt.show()
```

The `linestyle` parameter sets the style of the grid, the `linewidth` parameter sets the width of the grid line, and the `color` parameter sets the color of the grid.
