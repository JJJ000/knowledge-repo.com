---
title: Create a heatmap using a collection of scattered data
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To generate a heatmap using a scatter data set in Python, use the `hexbin()` function from the matplotlib library.
---

**Contents**

[TOC]

# Introduction
Heatmaps are useful tools for visualizing and analyzing large datasets. They can help identify patterns and trends within the data, making it easier to draw meaningful conclusions. In this tutorial, we will learn how to generate a heatmap using a scatter data set in Python.

# Getting Started
To begin, we need to import the necessary libraries. We will be using the pandas, numpy, and matplotlib libraries. If you do not already have them installed, you can install them using pip.

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```

Next, we need to create our scatter data set. For this tutorial, we will be using randomly generated data.

```python
# Create a scatter data set
x = np.random.randn(100)
y = np.random.randn(100)
```

# Creating the Heatmap
Now that we have our data set, we can create the heatmap. We will be using the hist2d function from matplotlib.

```python
# Create heatmap using hist2d function
plt.hist2d(x, y, bins=(20, 20), cmap=plt.cm.jet)
plt.colorbar()
plt.show()
```

The hist2d function takes in two arguments – the x and y data sets – as well as the number of bins to use for each axis and the color map to use. In this case, we are using 20 bins for each axis and the jet color map. We are also adding a color bar to the plot for reference.

# Conclusion
In this tutorial, we have learned how to generate a heatmap using a scatter data set in Python. Heatmaps are useful visualizations for large data sets and can help identify patterns and trends within the data. By using the hist2d function from the matplotlib library, we can create heatmaps quickly and easily in Python.
