---
title: How to reverse the x or y axis
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To invert the x or y axis in Python, use the pyplot.gca().invert\_xaxis() or pyplot.gca().invert\_yaxis() functions.
---

**Contents**

[TOC]

# Section 1: Matplotlib
Matplotlib is a Python library used for plotting data. It can be used to invert the x or y axis of a plot. To invert the x or y axis, you can use the `invert_xaxis()` or `invert_yaxis()` methods of the `Axes` object.

# Section 2: Example
The following example shows how to invert the x axis of a plot using Matplotlib.

```
import matplotlib.pyplot as plt

# Create a figure and an axes
fig, ax = plt.subplots()

# Plot some data
ax.plot([1,2,3,4])

# Invert the x axis
ax.invert_xaxis()

# Show the plot
plt.show()
```

# Section 3: Seaborn
Seaborn is another Python library used for plotting data. It can also be used to invert the x or y axis of a plot. To invert the x or y axis, you can use the `set_xscale()` or `set_yscale()` methods of the `Axes` object.

# Section 4: Example
The following example shows how to invert the y axis of a plot using Seaborn.

```
import seaborn as sns

# Create a figure and an axes
fig, ax = plt.subplots()

# Plot some data
sns.lineplot(x=[1,2,3,4], y=[1,2,3,4])

# Invert the y axis
ax.set_yscale('log')

# Show the plot
plt.show()
```
