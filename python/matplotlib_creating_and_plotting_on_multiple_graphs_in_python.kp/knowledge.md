---
title: What is the method to instruct matplotlib to generate a new plot, and subsequently plot on the previous one?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: You can create a second plot by calling the `subplots()` function, and plot on the old one again by using the `plt.plot()` function with the same axes object obtained from the `subplots()` call.
---

**Contents**

[TOC]

## Introduction

Matplotlib is a popular data visualization library in Python. It can create various types of plots such as line plots, scatter plots, bar plots, and more. In this tutorial, we will learn how to create multiple plots using Matplotlib in Python.

## Creating Multiple Plots

To create multiple plots, we can use the subplots() function of Matplotlib. This function creates a grid of plots with a specified number of rows and columns.

```python
import matplotlib.pyplot as plt

# create two plots
fig, (ax1, ax2) = plt.subplots(nrows=2, ncols=1)

# plot on the first plot
ax1.plot([1, 2, 3], [4, 5, 6])

# plot on the second plot
ax2.plot([1, 2, 3], [6, 5, 4])

plt.show()
```

In the above code, we create two subplots using the subplots() function with 2 rows and 1 column. We get the references to both the subplots using unpacking, and then we can plot on each of them using their respective references.

## Plotting on an Existing Plot

To plot on an existing plot, we simply reference the plot object and use its plotting functions. For example,

```python
import matplotlib.pyplot as plt

# create a plot
fig, ax = plt.subplots()

# plot on the first plot
ax.plot([1, 2, 3], [4, 5, 6])

# create a new plot
fig2, ax2 = plt.subplots()

# plot on the second plot
ax2.plot([1, 2, 3], [6, 5, 4])

# plot on the first plot again
ax.plot([4, 5, 6], [1, 2, 3])

plt.show()
```

In the above code, we first create a plot and plot some data on it. Then we create a new plot and plot some data on it as well. Then, we plot some more data on the first plot by referencing its plot object. Finally, we show both the plots using the show() function of Matplotlib.

## Conclusion

In this tutorial, we learned how to create multiple plots in Matplotlib and plot on an existing plot. With these techniques, we can create complex data visualizations that convey important insights.
