---
title: Creating a graph of (x, y) coordinates using matplotlib
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To plot a list of (x, y) coordinates in matplotlib in Python, use the scatter function.
---

**Contents**

[TOC]

# Introduction

When working with data, we often need to visualize it to gain insights and make it more interpretable. In Python, we can use the `matplotlib` library to create various types of plots, including scatter plots, which are useful for plotting (x, y) coordinates. In this article, we will look at how to plot a list of (x, y) coordinates using `matplotlib`.

# Imports

Before we start, we need to import the necessary libraries. We will use `matplotlib` for plotting and `numpy` for generating random data.

```python
import matplotlib.pyplot as plt
import numpy as np
```

# Generating Data

To plot a list of (x, y) coordinates, we first need to generate some data. We can use `numpy` to create random data. In this example, we will generate 50 points with random (x, y) coordinates between 0 and 1.

```python
# Generate random data
np.random.seed(0)
x = np.random.rand(50)
y = np.random.rand(50)
```

# Plotting Data

Now that we have generated our data, we can plot it using `matplotlib`. We can use the `scatter()` function to create a scatter plot of our points.

```python
# Create a scatter plot
plt.scatter(x, y)

# Set axis labels
plt.xlabel('X-axis')
plt.ylabel('Y-axis')

# Show plot
plt.show()
```

The `scatter()` function takes two arguments, `x` and `y`, which are the lists of x and y coordinates, respectively. We also set the axis labels using the `xlabel()` and `ylabel()` functions. Finally, we show our plot using the `show()` function.

# Conclusion

In this article, we have looked at how to plot a list of (x, y) coordinates using `matplotlib`. We first generated some random data using `numpy` and then created a scatter plot using the `scatter()` function. With this example, you can now plot your own (x, y) coordinate data for visualization and analysis.
