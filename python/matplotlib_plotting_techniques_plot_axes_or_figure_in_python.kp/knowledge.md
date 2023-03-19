---
title: Can you explain the contrast among utilizing plot, axes or figure for drawing plots in matplotlib?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Using plot creates a new figure and axes automatically, while axes and figure allow for more control over the placement and arrangement of multiple plots.
---

**Contents**

[TOC]

Introduction
------------

In `matplotlib`, there are different ways to draw plots including using `plot`, `axes`, and `figure`. While all of them serve to draw visualizations, they have different use cases and represent different elements of the plot. In this article, we'll discuss the differences between them.

Using `plot`
-------------

`Plot` is one of the most commonly used methods in `matplotlib` to draw plots. It is used to plot a single figure or a group of figures. By default, `plot` creates a figure and an `axes` and plots the data in them. The `plot` function is usually used for simple plots like line charts, scatter plots, histograms, and bar graphs.

Here's an example code that demonstrates how to use `plot`:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y)

plt.show()
```

This will output a line chart with five points.

Using `axes`
-------------

In `matplotlib`, an `axes` refers to the individual plot that we create. In other words, an `axes` is what we see when we plot something. `axes` is sometimes preferred over `plot` when we want to create multiple plots in the same figure. 

Here's an example code that demonstrates how to use `axes` to create a scatter plot and a line chart in the same figure:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.random.rand(100)
y = np.random.rand(100)

fig, (ax1, ax2) = plt.subplots(1, 2)
ax1.scatter(x, y)
ax2.plot(x, y)

plt.show()
```

This will create two plots side by side, one scatter plot `ax1` and one line chart `ax2`.

Using `figure`
--------------

`Figure` is the top-level container for all the elements that make up a `matplotlib` plot. Whenever we create a `plot` or an `axes`, a new `figure` is created. We can think of `figure` as the canvas that holds everything that we draw. 

`Figure` is generally used to customize the size, shape, and resolution of the entire image. It is usually used to create complex plots that consist of multiple subplots. 

Here's an example code that demonstrates how to use `figure` to create a complex figure with two subplots:

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 2 * np.pi, 400)
y = np.sin(x ** 2)

fig = plt.figure(figsize=(10,5))

ax1 = fig.add_subplot(121)
ax1.plot(x, y)

ax2 = fig.add_subplot(122, projection='3d')
ax2.scatter(x, y, x**2)

plt.show()
```

This will create a figure with two subplots, one line chart in 2D space, and one scatter plot in 3D space. 

Conclusion
----------

In a nutshell, `plot`, `axes`, and `figure` are three distinct methods available in `matplotlib`, each with its own use cases. `Plot` is used to create simple plots like line charts, scatter plots, histograms, and bar graphs. `Axes` is used to create multiple plots in the same figure. `Figure` is used to create complex plots that consist of multiple subplots. By understanding their differences and use cases, we can create beautiful visualizations in `matplotlib`.
