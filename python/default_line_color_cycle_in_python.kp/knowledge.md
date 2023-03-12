---
title: Retrieve the default cycle of line colors
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The default line color cycle in Python is a sequence of ten colors that are cycled through when plotting multiple lines without specifying the color explicitly.
---

**Contents**

[TOC]

## Introduction
When plotting multiple lines using matplotlib library in Python, it's important to have a distinct colour for each line in the plot. Matplotlib library automatically chooses the colour for the plot when using different plot commands repeatedly. However, sometimes it's important to understand the default colour cycle used by matplotlib for plotting different lines.

## Accessing default line colour cycle
Default line colour cycle used by matplotlib can be accessed by using `prop_cycler` module of the `matplotlib.rcParams` module:

```python
import matplotlib.pyplot as plt

# Get default colour cycle 
default_cycler = plt.rcParams['axes.prop_cycle']
print(default_cycler)
```

This will return the default color cycle used by matplotlib for plotting different lines.

## Using default line colour cycle
Default line color cycle can be used to customize the color of different lines in the plot, as shown below:

```python
import numpy as np
import matplotlib.pyplot as plt

# Creating random data
x = np.arange(0, 10, 1)
y1 = np.random.rand(10)
y2 = np.random.rand(10)

# Get default color cycle
default_cycler = plt.rcParams['axes.prop_cycle']

# Plotting lines with default color cycle
fig, ax = plt.subplots()
ax.set_prop_cycle(default_cycler)
ax.plot(x, y1)
ax.plot(x, y2)

plt.show()
```
In this example, we've used the default color cycle to plot multiple lines with custom line colors.

## Modifying default line colour cycle
You can also modify the default line color cycle using the `set_prop_cycle` method of `matplotlib.pyplot` as shown below:

```python
import numpy as np
import matplotlib.pyplot as plt

# Creating random data
x = np.arange(0, 10, 1)
y1 = np.random.rand(10)
y2 = np.random.rand(10)

# Modifying default colour cycle 
new_cycler = plt.cycler(color=["r", "g", "b"])
plt.rcParams["axes.prop_cycle"] = new_cycler

# Plotting lines with modified color cycle
fig, ax = plt.subplots()
ax.plot(x, y1)
ax.plot(x, y2)

plt.show()
```

In this example, we modified the default color cycle by creating a new color cycle with only three colors ("red", "green", and "blue") and then setting it as the new default color cycle. This custom color cycle will be used for all subsequent plots using matplotlib.
