---
title: Keep the axis labels but conceal the values of tick labels
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To hide tick label values but keep axis labels in Python, you can set the tick label values to an empty list using plt.xticks([]) or ax.set\_xticklabels([]) if using an axis object.
---

**Contents**

[TOC]

# Introduction

In data visualization, sometimes we need to hide the tick label values in our plot but still want to keep the axis labels. In this article, we will discuss how to achieve this in Python using matplotlib.

# Example Data

Let's first create some example data to use for plotting:

```python
import numpy as np

x = np.arange(0, 10, 0.5)
y = np.sin(x)
```

# Solution: Using `set_ticklabels()` Method

We can achieve hiding the tick label values while keeping the axis labels by setting the tick label values to an empty list using the `set_ticklabels()` method of the `matplotlib` axis object.

```python
import matplotlib.pyplot as plt

fig, ax = plt.subplots()

ax.plot(x, y)

ax.set_xticklabels([])
ax.set_yticklabels([])

plt.show()
```

In the above code, we first create a figure and an axis object using the `subplots()` method of the `matplotlib.pyplot` module. Then we plot our data on the axis object using the `plot()` method.

Next, we use the `set_xticklabels([])` and `set_yticklabels([])` methods of the `ax` object to set the tick label values to an empty list. This hides the tick label values on both x-axis and y-axis while keeping the axis labels.

Finally, we use the `show()` method of the `matplotlib.pyplot` module to display the plot.


# Solution: Using `tick_params()` Method

Another way to achieve the same result is by using the `tick_params()` method of the `matplotlib` axis object. Here's how:

```python
fig, ax = plt.subplots()

ax.plot(x, y)

ax.tick_params(axis='both', which='both', length=0)

plt.show()
```

In the above code, we use the `tick_params()` method with `axis='both'` and `which='both'` arguments to set the properties of both x and y axis. We set the `length` property to 0 to hide the tick labels.

Finally, we use the `show()` method of the `matplotlib.pyplot` module to display the plot.


# Conclusion

In this article, we discussed two ways to hide the tick label values but still keep the axis labels in a Python plot using Matplotlib - using `set_ticklabels()` method and `tick_params()` method. These methods can be used to improve the readability and aesthetics of plots as required for various data visualization applications.
