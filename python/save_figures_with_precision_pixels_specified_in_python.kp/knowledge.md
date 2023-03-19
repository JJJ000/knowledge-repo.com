---
title: Describing and preserving a figure with an exact size in pixels
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use `fig.set\_size\_inches` method to specify the size of the figure in pixels and save it using `plt.savefig` method in Python.
---

**Contents**

[TOC]

Section 1: Introduction
In data science and visualization, figures play a crucial role in representing the insights and patterns in the data. However, sometimes it becomes necessary to specify and save the figures with exact size in pixels. In this article, we will discuss how to achieve this in Python.

Section 2: Creating a Figure with Specific Size
To create a figure with specific size in pixels, we need to use the `figure` function from the matplotlib library. The `figure` function accepts `figsize` parameter, which is a tuple of width and height in inches.

```python
import matplotlib.pyplot as plt

fig = plt.figure(figsize=(width_in_pixels/100, height_in_pixels/100), dpi=100)
```

Here, we divide the width and height in pixels with 100 to convert them into inches, and set the `dpi` (dots per inch) parameter to 100 for better image quality. 

Section 3: Saving the Figure with Specific Size
To save the figure with specific size, we need to call the `savefig` function from the matplotlib library. The `savefig` function accepts the `dpi` parameter, which sets the resolution of the image in dots per inch.

```python
fig.savefig('figure.png', dpi=100)
```

Here, we save the figure as `figure.png` with a resolution of 100 dots per inch.

Section 4: Conclusion
In this article, we discussed how to create and save a figure with specific size in pixels in Python. By setting the `figsize` parameter of `figure` function and `dpi` parameter of `savefig` function, we can achieve the desired image size and resolution.
