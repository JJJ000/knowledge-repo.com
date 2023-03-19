---
title: What is the method for exporting matplotlib plots with a clear background?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Set the background color to `none` and save the figure with the alpha parameter as `png` or `svg` file format.
---

**Contents**

[TOC]

## 1. Setting the transparent background

To set a transparent background in matplotlib, we need to modify the alpha value of the `facecolor` property of the figure. We can set this value to 0 to make the background fully transparent, or any value between 0 and 1 to make it partially transparent. 

```python
import matplotlib.pyplot as plt

# Create a figure
fig = plt.figure()

# Set alpha value of facecolor to make it transparent
fig.patch.set_facecolor('none')
```

## 2. Saving the plot with transparent background

To save the plot with a transparent background, we need to use the `savefig` function in matplotlib and provide a file extension that supports transparency, such as `.png`.

```python
# Create a plot
plt.plot([1, 2, 3], [4, 5, 6])

# Save the plot with transparent background
plt.savefig('plot.png', transparent=True)
```

## 3. Example code

Here's a complete example code that demonstrates how to create a plot with a transparent background and save it as a PNG file:

```python
import numpy as np
import matplotlib.pyplot as plt

# Create sample data
x = np.arange(0, 5, 0.1)
y = np.sin(x)

# Create a figure
fig = plt.figure()

# Set alpha value of facecolor to make it transparent
fig.patch.set_facecolor('none')

# Create a plot
plt.plot(x, y)

# Save the plot with transparent background
plt.savefig('plot.png', transparent=True)
```

## 4. Result

The resulting PNG file will have a transparent background, which means that it can be easily overlaid on top of other images or used in presentations without any distracting background.
