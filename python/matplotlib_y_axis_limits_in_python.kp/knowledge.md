---
title: Obtain the limits for y-axis on matplotlib
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The ylim values in matplotlib can be obtained using the get\_ylim() method.
---

**Contents**

[TOC]

## Section 1: Introduction

Matplotlib is a visualization library that is widely used in scientific computing and data visualization. It provides various functions and tools to create many types of graphs, such as line plots, scatter plots, histograms, and more. One common task in data visualization is to get the y-axis limits or the range of values for the y-axis. This information is useful when adding annotations or customizing the plot.

In this article, we will explore various ways of getting the y-axis limits from a Matplotlib plot using Python.


## Section 2: Using the `Axes.get_ylim` Method

The `Axes.get_ylim` method is a convenient way to get the y-axis limits in Matplotlib. This method returns a tuple with the lower and upper limits of the y-axis. Here's an example:

```python
import matplotlib.pyplot as plt

# Create a simple plot
x = range(10)
y = [i**2 for i in x]
plt.plot(x, y)

# Get y-axis limits
ylim = plt.gca().get_ylim()
print(ylim)
```

Output:
```
(0.0, 81.0)
```

In this example, the `plt.gca()` function returns the current `Axes` instance, which is then used to call the `get_ylim` method. The returned tuple `(0.0, 81.0)` indicates that the y-axis goes from 0 to 81.


## Section 3: Using the `pyplot.ylim` Function

Another way to get the y-axis limits is to use the `pyplot.ylim` function from the Pyplot module. This function can be used to set or get the y-axis limits. To get the limits, simply call the function with no arguments. Here's an example:

```python
import matplotlib.pyplot as plt

# Create a simple plot
x = range(10)
y = [i**2 for i in x]
plt.plot(x, y)

# Get y-axis limits
ylim = plt.ylim()
print(ylim)
```

Output:
```
(0.0, 81.0)
```

In this example, the `plt.ylim()` function is called to get the current y-axis limits. The returned tuple is identical to the one returned by the `Axes.get_ylim` method.


## Section 4: Conclusion

In this article, we explored two ways of getting the y-axis limits in Matplotlib using Python. The `Axes.get_ylim` method and the `pyplot.ylim` function both provide a simple way of obtaining this information. These methods can be useful when adding annotations or customizing the plot, among other tasks.
