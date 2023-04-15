---
title: Adjust the size of the colorbar in matplotlib to match that of the graph
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `shrink` parameter in `colorbar()` function to scale down the colorbar to match the size of the graph.
---

**Contents**

[TOC]

### Section 1: Introduction

Matplotlib is a Python library used for data visualization. It provides extensive support for creating graphs, plots, and charts. One of the features it provides is the ability to create colorbars on a graph. A colorbar is a representation of the color gradient used in the graph. However, the size of the colorbar may not match the size of the graph, making it look disproportionate. In this tutorial, we will discuss how to set the Matplotlib colorbar size to match the graph in Python.

### Section 2: Creating a graph with a colorbar

Before we learn how to set the Matplotlib colorbar size to match the graph, let's first create a graph with a colorbar. The following code will create a scatter plot with a colorbar:

```
import matplotlib.pyplot as plt
import numpy as np

x = np.random.randn(1000)
y = np.random.randn(1000)
colors = np.random.rand(1000)

fig, ax = plt.subplots()
sc = ax.scatter(x, y, c=colors, cmap='viridis')
plt.colorbar(sc)

plt.show()
```

### Section 3: Resizing the colorbar

The default size of the colorbar is not always ideal. We can adjust the size of the colorbar to match the size of the graph. To do so, we need to do two things:

- Set the size of the colorbar using the `shrink` parameter
- Adjust the size of the graph to make room for the colorbar

Here's how we can adjust the size of the colorbar:

```
import matplotlib.pyplot as plt
import numpy as np

x = np.random.randn(1000)
y = np.random.randn(1000)
colors = np.random.rand(1000)

fig, ax = plt.subplots()
sc = ax.scatter(x, y, c=colors, cmap='viridis')
cbar = plt.colorbar(sc, shrink=0.6)  # adjust the size using the shrink parameter

plt.show()
```

In this example, we set the `shrink` parameter to 0.6. This means that the colorbar will be 60% of its original size.

### Section 4: Adjusting the graph size

The colorbar takes up space on the graph, so we need to adjust the size of the graph to make room for it. We can do this by setting the figure size when we create the `fig` object.

Here's how we can set the figure size:

```
import matplotlib.pyplot as plt
import numpy as np

x = np.random.randn(1000)
y = np.random.randn(1000)
colors = np.random.rand(1000)

fig, ax = plt.subplots(figsize=(8, 6))  # set the figure size
sc = ax.scatter(x, y, c=colors, cmap='viridis')
cbar = plt.colorbar(sc, shrink=0.6)

plt.show()
```

In this example, we set the `figsize` parameter to `(8,6)`. This means that the graph will have a width of 8 inches and a height of 6 inches. Now the colorbar is proportional to the graph, and everything looks aesthetically pleasing.
