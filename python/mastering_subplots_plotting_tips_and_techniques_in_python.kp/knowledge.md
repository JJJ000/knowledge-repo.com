---
title: What is the method for creating multiple subplots?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the subplots() function from matplotlib module to create multiple subplots and plot on each individual subplot using its respective axis.
---

**Contents**

[TOC]

## Section 1: Introduction
Plotting multiple subplots in a single figure is often useful for comparing data and gaining insights from the visualizations. Python provides us with a variety of libraries for creating multi-plot figures, including matplotlib, seaborn, and plotly.

In this tutorial, we will focus on using the matplotlib library to create and customize subplots.

## Section 2: Creating subplots
The first step in creating subplots is to create a figure object using the `figure()` function of matplotlib. The `figure()` function takes several optional arguments where we can customize the figure size and other properties.

Once we have the figure object, we can create subplots using the `subplots()` function. The `subplots()` function takes several arguments where we can specify the number of rows and columns of the subplot grid, and the overall figure size. 

Here is an example code that creates a 2x2 grid of subplots:

```python
import matplotlib.pyplot as plt

fig = plt.figure(figsize=(8, 8))

# create a 2x2 grid of subplots
ax1 = fig.add_subplot(2, 2, 1)
ax2 = fig.add_subplot(2, 2, 2)
ax3 = fig.add_subplot(2, 2, 3)
ax4 = fig.add_subplot(2, 2, 4)
```

In the above example, we created a figure object of size 8x8 inches and then used the `add_subplot()` function to create a 2x2 grid of subplots. We assigned each subplot object to a variable (`ax1`, `ax2`, `ax3`, and `ax4`) that we can use to customize each subplot individually.

## Section 3: Customizing subplots
Once we have created the subplots, we can customize each subplot by calling various methods on the subplot objects.

For example, we can set the title and axis labels of the subplot using the following methods:

```python
ax1.set_title("Subplot 1")
ax1.set_xlabel("X Label")
ax1.set_ylabel("Y Label")
```

We can also plot data on each subplot using various plotting functions provided by matplotlib. Here is an example code that plots a scatter plot on the first subplot:

```python
import numpy as np

# generate some random data
x = np.random.rand(100)
y = np.random.rand(100)

# plot a scatter plot on the first subplot
ax1.scatter(x, y)
```

In the above code, we generated some random data and then plotted a scatter plot on the first subplot using the `scatter()` function of `ax1`.

## Section 4: Saving subplots
Once we have customized the subplots to our liking, we can save the figure using the `savefig()` function of matplotlib. The `savefig()` function takes a filename and optional arguments where we can specify the file format, DPI, and other properties.

Here is an example code that saves the figure as a PNG file:

```python
fig.savefig("subplots.png", dpi=300)
```

In the above example, we saved the figure as a PNG file named "subplots.png" with a resolution of 300 DPI. We can choose other file formats like JPG, PDF, SVG, etc. by changing the filename extension.
