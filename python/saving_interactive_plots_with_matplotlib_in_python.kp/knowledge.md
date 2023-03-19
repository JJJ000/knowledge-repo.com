---
title: The action of preserving matplotlib figures that have interactive capabilities
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `savefig()` function in Matplotlib to save interactive figures in various file formats such as PNG, PDF, SVG, etc.
---

**Contents**

[TOC]

Section 1: Introduction to Matplotlib 
Matplotlib is a powerful data visualization library in Python that provides several plotting tools for generating 2D graphs, bar charts, heatmap, etc. The library is widely used by data scientists and researchers for representing their data graphically.

Section 2: Creating Interactive Matplotlib Figures 
Matplotlib provides several interactive tools that allow users to modify, zoom, save or view the plot. One such tool is the NavigationToolbar2TkAgg that provides several buttons for working with the plot. To create an interactive plot, we must first import the required modules as follows:

```
import matplotlib.pyplot as plt
from matplotlib.backends.backend_tkagg import NavigationToolbar2Tk

```
Next, we create a figure, a subplot, and some data to plot. Finally, we add the NavigationToolbar2Tk to the graph as shown below:

```
fig, ax = plt.subplots(1, 1)
ax.plot([1, 2, 3], [2, 3, 4])

toolbar = NavigationToolbar2Tk(fig.canvas, root)
toolbar.update()
fig.canvas.toolbar = toolbar

```
The above code creates a single axis graph that plots the data [1,2,3] vs [2,3,4]. The NavigationToolbar2Tk is then added to the plot.

Section 3: Saving Interactive Matplotlib Figures 
Matplotlib provides several methods for saving interactive figures such as PDF, JPEG, PNG, etc. Saving interactive Matplotlib figures requires the use of the pillow library. Pillow is a powerful image processing library in Python that allows interactive figures to be saved to disk. To save an interactive figure, we must first import the required modules as follows:

```
from PIL import Image
```
Next, we get the current canvas and save the image to disk as shown below:

```
canvas = fig.canvas

canvas.draw()

image = Image.frombytes('RGB', canvas.get_width_height(),
                         canvas.tostring_rgb())

image.save("my_figure.jpg", "JPEG")

```

The above code gets the current canvas and saves the image as a JPEG file to disk. We can also save the image as a PDF or PNG file by changing the file extension.

Section 4: Conclusion 
Interactive figures are a great way to explore and visualize data. Matplotlib provides several interactive tools that allow users to modify, zoom, save or view the plot. We can save interactive figures to disk using Pillow library.
