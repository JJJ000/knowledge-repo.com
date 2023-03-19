---
title: Assign labels to specific points on a matplotlib line
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: To set markers for individual points on a line in Matplotlib in Python, use the `marker` parameter when plotting the line with the specific marker style for each point.
---

**Contents**

[TOC]

Section 1: Introduction
Matplotlib is a popular data visualization library in Python. It provides several types of plots to represent data, including line plots. Line plots are useful for showing trends in data over time or across different categories. Sometimes we need to highlight specific points on a line to draw attention to them. In this tutorial, we will explore how to set markers for individual points on a line in Matplotlib.

Section 2: Creating a basic line plot
Before we can set markers for individual points on a line, we need to create a basic line plot. We will use the Matplotlib.pyplot module to create a line plot of two lists, x and y.

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [10, 8, 6, 4, 2]

plt.plot(x, y)
plt.show()
```

The code above creates a simple line plot with x values on the horizontal axis and y values on the vertical axis.

Section 3: Setting markers for individual points on a line
To set markers for individual points on a line, we need to use the `marker` parameter in the `plt.plot()` function. We can specify the type of marker using a string argument.

```python
plt.plot(x, y, marker='o')
plt.show()
```

In the code above, we added the `marker='o'` parameter to the `plt.plot()` function, which tells Matplotlib to use circles as markers for each point on the line.

We can also change the size and color of the markers using additional parameters.

```python
plt.plot(x, y, marker='o', markersize=10, markerfacecolor='red')
plt.show()
```

In the code above, we set the `markersize` parameter to 10 and the `markerfacecolor` parameter to 'red'. This creates larger circles with a red color for each point on the line.

Section 4: Setting markers for specific points on a line
To set markers for specific points on a line, we need to create a list of the same length as the x and y lists and specify the marker for each point using the list.

```python
markers = ['o', 's', '^', 'D', 'v']

plt.plot(x, y, marker='o', markersize=10, markerfacecolor='red', markevery=markers)
plt.show()
```

In the code above, we created a list of markers called `markers` and specified the `markevery` parameter to use the markers list for each point on the line. This creates circles, squares, triangles, diamonds, and down-pointing triangles for each point on the line.

We can also set different marker styles and sizes for specific points using separate lists for the `markevery`, `markersize`, and `markerfacecolor` parameters.

```python
markers = ['o', 's', '^', 'D', 'v']
sizes = [10, 20, 30, 40, 50]
colors = ['red', 'blue', 'green', 'orange', 'purple']

plt.plot(x, y, marker='o', markersize=10, markerfacecolor='gray', markevery=markers, markersize=sizes, markerfacecolor=colors)
plt.show()
```

In the code above, we created separate lists for `markevery`, `markersize`, and `markerfacecolor` and specified them as parameters in the `plt.plot()` function. This creates a line plot with different markers, sizes, and colors for each point on the line.
