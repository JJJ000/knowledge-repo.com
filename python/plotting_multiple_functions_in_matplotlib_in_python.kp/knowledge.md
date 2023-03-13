---
title: What is the method for plotting multiple functions on a single figure in matplotlib?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `plt.plot()` function multiple times with different data for each function, followed by `plt.show()` to display the figure.
---

**Contents**

[TOC]

## Introduction

Matplotlib is a powerful visualization library for creating professional-grade plots in Python. It is widely used among data scientists, researchers, and engineers. One of its most powerful features is the ability to plot multiple functions on the same figure. In this guide, we'll show you how to do just that.

## Section 1: Importing Matplotlib

The first thing we need to do is import Matplotlib. In this example, we'll import the pyplot module, which provides a simple interface for creating plots.

```python
import matplotlib.pyplot as plt
```

## Section 2: Creating the Functions

Now that we've imported Matplotlib, we can define our functions. For this example, we'll create two simple functions to plot.

```python
import numpy as np

def f(x):
    return np.sin(x)

def g(x):
    return np.cos(x)
```

These functions will provide the y-values for our plot.

## Section 3: Creating the Plot

With our functions defined, we can now create the plot. We'll start by creating an array of x-values to plot.

```python
x = np.linspace(0, 2*np.pi, 1000)
```

This creates 1000 evenly spaced x-values between 0 and 2*pi. We can now plot our functions and label them.

```python
plt.plot(x, f(x), label='sin(x)')
plt.plot(x, g(x), label='cos(x)')
```

Finally, we'll add a legend to the plot and show it.

```python
plt.legend()
plt.show()
```

## Conclusion

In this guide, we've shown how to plot multiple functions on the same figure using Matplotlib. By defining our functions and creating a plot, we can easily visualizes multiple functions in a single plot. Matplotlib is a powerful tool for data visualization that offers a lot of customization options.
