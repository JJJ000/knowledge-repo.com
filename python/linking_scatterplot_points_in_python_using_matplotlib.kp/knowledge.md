---
title: How to link the points in a scatter plot using lines in Python with matplotlib?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To connect scatterplot points with a line in Matplotlib library of Python, set the `linestyle` attribute in the `plot` function to `-` or any other appropriate value.
---

**Contents**

[TOC]

Section 1: Introduction
Matplotlib is one of the most widely used visualization libraries in Python. It provides powerful tools for creating a wide range of visualizations such as line graphs, scatter plots, and bar charts. In this tutorial, we will show you how to connect scatterplot points with a line in Python using Matplotlib.

Section 2: Creating a Scatterplot
The first step in creating a scatterplot is to import the required libraries. We will be using NumPy and Matplotlib for this example. Once the libraries are imported, we can generate random data to plot using the following code:

```python
import numpy as np
import matplotlib.pyplot as plt

# Generate random data
x = np.random.randn(50)
y = np.random.randn(50)

# Create scatterplot
plt.scatter(x, y)
```

The above code creates a scatter plot with 50 random x and y values.

Section 3: Connecting Points with Lines
To connect the scatter plot points with lines, we need to add a line plot on top of the scatter plot. We can achieve this by creating another variable that contains the x and y values and then plotting it using the `plot()` function.

```python
import numpy as np
import matplotlib.pyplot as plt

# Generate random data
x = np.random.randn(50)
y = np.random.randn(50)

# Create scatterplot
plt.scatter(x, y)

# Connect points with a line
plt.plot(x, y)
```

The above code will plot a scatter plot with points connected by lines.

Section 4: Customizing the Plot
We can further customize the plot by changing the line style, color, and thickness. The following code shows an example of changing the line style to dotted, the color to red, and the thickness to 2.

```python
import numpy as np
import matplotlib.pyplot as plt

# Generate random data
x = np.random.randn(50)
y = np.random.randn(50)

# Create scatterplot
plt.scatter(x, y)

# Connect points with a line
plt.plot(x, y, linestyle=':', color='red', linewidth=2)

plt.show()
```

The above code will plot a scatter plot with points connected by a red, dotted line of thickness 2.
