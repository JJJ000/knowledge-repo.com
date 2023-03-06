---
title: Decreasing the quantity of ticks on the plot
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `set\_xticks` and `set\_yticks` methods of the `matplotlib.pyplot` module to manually specify a smaller set of tick values on the x and/or y axis.
---

**Contents**

[TOC]

## Introduction

When visualizing data, it is often necessary to adjust the number of ticks on the x and y axes. While having more ticks can offer a more detailed view of the data, it can also make the plot cluttered and difficult to read. Conversely, having too few ticks can make it difficult to pinpoint specific data points. In this guide, we will explore different methods to reduce the number of plot ticks in Python.

## Method 1: Manually setting the ticks

The most straightforward way to reduce the number of ticks on a plot is to manually set them using the `xticks()` and `yticks()` functions. These functions take a list of values to use as tick marks. We can use the `linspace()` function from the `numpy` library to generate evenly spaced values to use as ticks. 

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.arange(0, 10, 0.1)
y = np.sin(x)

plt.plot(x, y)
plt.xticks(np.linspace(0, 10, 5))
plt.yticks(np.linspace(-1, 1, 3))
plt.show()
```

In this example, we generate five evenly spaced ticks on the x-axis between 0 and 10, and three on the y-axis between -1 and 1.

## Method 2: Using MaxNLocator

We can also adjust the number of ticks using the `MaxNLocator` class from the `matplotlib.ticker` module. This class automatically adjusts the number of ticks based on the range of values to be shown. By default, it will generate between 5 and 9 ticks.

```python
import matplotlib.pyplot as plt
import numpy as np
import matplotlib.ticker as ticker

x = np.arange(0, 10, 0.1)
y = np.sin(x)

fig, ax = plt.subplots()
ax.plot(x, y)

# Set the x-axis locator to work with MaxNLocator
ax.xaxis.set_major_locator(ticker.MaxNLocator(5))

plt.show()
```

In this example, we set the `xaxis` locator to `MaxNLocator(5)`, which will generate up to 5 ticks on the x-axis.

## Method 3: Using AutoLocator

Another option is to use the `AutoLocator` class from the `matplotlib.ticker` module. This class automatically adjusts the number of ticks based on the size of the axis and the range of values to be shown. 

```python
import matplotlib.pyplot as plt
import numpy as np
import matplotlib.ticker as ticker

x = np.arange(0, 10, 0.1)
y = np.sin(x)

fig, ax = plt.subplots()
ax.plot(x, y)

# Set the x-axis locator to work with AutoLocator
ax.xaxis.set_major_locator(ticker.AutoLocator())

plt.show()
```

In this example, we set the `xaxis` locator to `AutoLocator()`, which will automatically generate an appropriate number of ticks based on the range of values to be shown.

## Conclusion

In summary, there are several ways to reduce the number of ticks on a plot in Python. We can manually set the ticks, use `MaxNLocator` or `AutoLocator` to automatically adjust the number of ticks based on the range of values to be shown. It's important to find the appropriate balance between having enough information and keeping the plot clean and readable. The choice will also depend on the type of data and the context of visualization.
