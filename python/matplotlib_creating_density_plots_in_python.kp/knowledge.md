---
title: What are the steps to generate a density plot using matplotlib?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the seaborn library to create a kernel density estimate plot using the kdeplot() function.
---

**Contents**

[TOC]

## Introduction

A density plot or kernel density estimate plot (KDE) is a graphical representation of the probability density function of a continuous random variable. It is used to visualize the distribution of data over a continuous interval. In this tutorial, we will learn how to create a density plot in matplotlib in Python.


## Importing Libraries

To create a density plot in Python, we need to import the required libraries. We will use the NumPy and Matplotlib library.

```python
import numpy as np
import matplotlib.pyplot as plt
```

## Generating Data

For creating a density plot, we need some data to plot. We can use the NumPy library to generate some random data.

```python
# Generate random data
data = np.random.normal(size=1000)
```

## Creating a Density Plot

Now, we can create a density plot using the `plt.plot()` function in matplotlib. We can specify the `kind` parameter as `density` to create a density plot.

```python
# Plot the density plot
plt.hist(data, density=True)
plt.show()
```

This will create a density plot for the random data generated. We can customize our density plot by changing the number of bins, setting the color of the plot, adding labels to the axes, and adding a title to the plot.

```python
# Customizing the density plot
plt.hist(data, bins=30, density=True, color='orange')
plt.xlabel('Data')
plt.ylabel('Probability Density')
plt.title('Density Plot')
plt.show()
```

This will create a customized density plot with 30 bins, orange color, labeled axes, and a title for the plot. 

## Conclusion

In this tutorial, we learned how to create a density plot in matplotlib using the NumPy and Matplotlib library. We generated some random data and used the `plt.plot()` function to create a density plot. We also customized the plot by changing the number of bins, plot color, adding labels and a title to the plot. Density plot is a useful tool to visualize the distribution of data over a continuous interval.
