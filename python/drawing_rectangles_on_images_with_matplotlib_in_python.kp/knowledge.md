---
title: Can you provide instructions on how to depict a rectangle on an image using matplotlib?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the matplotlib.pyplot.Rectangle() function to draw a rectangle on an image in Python.
---

**Contents**

[TOC]

# Introduction
Sometimes, we need to draw a rectangle on an image using Python. This task can be accomplished with the help of the Python library known as Matplotlib. In this tutorial, we will learn how to draw a rectangle on an image using Matplotlib.

# Section-1: Load image using Matplotlib
Before we can draw a rectangle on an image, we need to load the image into Matplotlib. Matplotlib can load a variety of image formats, including JPEG, PNG, BMP, and GIF. The following code snippet shows how to load an image into Matplotlib.

``` python
import matplotlib.pyplot as plt
import matplotlib.image as mpimg

# Load image using Matplotlib
image = mpimg.imread('path/to/image.jpg')

# Show image
plt.imshow(image)
```

# Section-2: Draw a rectangle on image using Matplotlib
After we have loaded the image into Matplotlib, we can draw a rectangle on the image using the `Rectangle` class of Matplotlib. The `Rectangle` class represents a rectangle with its bottom-left corner at `(x, y)` and height `height` and width `width`. The following code snippet shows how to draw a rectangle on an image using Matplotlib.

``` python
import matplotlib.pyplot as plt
import matplotlib.image as mpimg
from matplotlib.patches import Rectangle

# Load image using Matplotlib
image = mpimg.imread('path/to/image.jpg')

# Create figure and axes
fig, ax = plt.subplots()

# Show image on axes
ax.imshow(image)

# Create rectangle
rect = Rectangle((x, y), width, height, fill=False, color='red')

# Add rectangle to axes
ax.add_patch(rect)

# Show image with rectangle
plt.show()
```

# Section-3: Customize rectangle properties
We can customize the properties of the rectangle, such as its color, width, and transparency. The following code snippet shows how to change the color and width of the rectangle.

``` python
# Create a thick red rectangle
rect = Rectangle((x, y), width, height, fill=False, edgecolor='red', linewidth=2)
```

# Section-4: Conclusion
In this tutorial, we learned how to draw a rectangle on an image using Matplotlib. We first loaded the image into Matplotlib and then used the `Rectangle` class to draw a rectangle on the image. We also learned how to customize the properties of the rectangle, such as its color and width.
