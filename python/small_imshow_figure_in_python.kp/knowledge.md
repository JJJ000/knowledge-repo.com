---
title: The size of the imshow() object is insufficiently large
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You can increase the size of the figure using matplotlib`s `figure()` function.
---

**Contents**

[TOC]

# Introduction
In data visualization, `imshow()` is a commonly used function to display images or arrays as an image. However, sometimes the figure produced by `imshow()` is too small, making it difficult to interpret the data. In this article, we will discuss some possible reasons why this problem occurs and how to solve it.


# Reason 1: Default Figure Size
The default figure size in `imshow()` might be too small for the size of the array. In this case, we can adjust the figure size using the `figure()` function before calling `imshow()`. For example:

```
import matplotlib.pyplot as plt
import numpy as np

# create a random 10x10 array
arr = np.random.rand(10, 10)

# set figure size to 8x6
plt.figure(figsize=(8, 6))

# display the array as an image
plt.imshow(arr)

# show the plot
plt.show()
```

In this example, we set the figure size to 8x6 (in inches) before calling `imshow()`.


# Reason 2: Aspect Ratio
Another possible reason why the figure produced by `imshow()` is too small is that the aspect ratio of the plot is not appropriate for the array. By default, `imshow()` sets the aspect ratio to be equal to the ratio of the width and height of the array. However, if the array is not square, this might result in a figure that is too small.

To solve this problem, we can set the aspect ratio of the plot manually using the `aspect` parameter. For example:

```
import matplotlib.pyplot as plt
import numpy as np

# create a random 10x20 array
arr = np.random.rand(10, 20)

# set figure size to 8x6
plt.figure(figsize=(8, 6))

# set aspect ratio to 0.5
plt.imshow(arr, aspect=0.5)

# show the plot
plt.show()
```

In this example, we set the aspect ratio to 0.5, which means that the width of the plot will be twice the height.


# Reason 3: Displaying Multiple Arrays
A third reason why the figure produced by `imshow()` might be too small is that we are displaying multiple arrays in the same plot. In this case, we can use the `subplot()` function to create a grid of subplots and display each array in a different subplot. For example:

```
import matplotlib.pyplot as plt
import numpy as np

# create two random 10x10 arrays
arr1 = np.random.rand(10, 10)
arr2 = np.random.rand(10, 10)

# set figure size to 8x6
plt.figure(figsize=(8, 6))

# create a grid of subplots
plt.subplot(1, 2, 1)
plt.imshow(arr1)

plt.subplot(1, 2, 2)
plt.imshow(arr2)

# show the plot
plt.show()
```

In this example, we use `subplot()` to create a grid of two subplots, and we display each array in a different subplot.


# Conclusion
In this article, we discussed some possible reasons why the figure produced by `imshow()` might be too small and how to solve these problems. By adjusting the figure size, aspect ratio, and using subplots, we can create figures that are easy to interpret and display our data effectively.
