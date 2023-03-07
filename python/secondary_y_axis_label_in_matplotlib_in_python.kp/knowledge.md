---
title: Modifying matplotlib to label the y-axis for a secondary y-axis
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the set\_ylabel() method on the axis object for the secondary y-axis.
---

**Contents**

[TOC]

Section 1: Introduction
In this tutorial, we will discuss how to add a y-axis label to the secondary y-axis in Matplotlib in Python. Matplotlib is a popular data visualization library used in Python. It provides various types of graphs and charts for data visualization.

Section 2: Creating a Secondary Y-axis
To create a secondary y-axis in Matplotlib, we need to first create a figure and then add two subplots. In this example, we will create two subplots, one for the primary y-axis and the other for the secondary y-axis.

```python
import matplotlib.pyplot as plt
import numpy as np

# create a figure with two subplots
fig, ax1 = plt.subplots()

# create a second subplot with the same x-axis
ax2 = ax1.twinx()
```

The `twinx()` method creates a second y-axis with the same x-axis as the first y-axis.

Section 3: Adding a Y-axis Label to Secondary Y-axis
To add a y-axis label to the secondary y-axis, we need to use the `set_ylabel()` method. This method takes a string as the label text.

```python
# set the label for the primary y-axis
ax1.set_ylabel('Primary Axis Label')

# set the label for the secondary y-axis
ax2.set_ylabel('Secondary Axis Label')
```

This will add two y-axis labels to the subplots. The `set_ylabel()` method can also be used to set the properties of the label such as the font size, font style, font color, etc.

Section 4: Example Code
Here is the complete code to create a secondary y-axis and add y-axis labels:

```python
import matplotlib.pyplot as plt
import numpy as np

# create a figure with two subplots
fig, ax1 = plt.subplots()

# create a second subplot with the same x-axis
ax2 = ax1.twinx()

# plot some data on both axes
x = np.linspace(0, 10, 100)
ax1.plot(x, np.sin(x), 'b-')
ax2.plot(x, np.cos(x), 'r-')

# set the label for the primary y-axis
ax1.set_ylabel('Primary Axis Label')

# set the label for the secondary y-axis
ax2.set_ylabel('Secondary Axis Label')

# show the plot
plt.show()
```

This code will create two subplots, plot sine and cosine wave data on both axes, add y-axis labels to both axes, and display the plot.
