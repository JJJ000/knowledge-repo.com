---
title: How can the "camera position" be configured for 3d plots in python/matplotlib?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Set the camera position for 3D plots in Python/Matplotlib using the `view\_init` function.
---

**Contents**

[TOC]

## Introduction 
Setting the camera position is an essential aspect of creating a three-dimensional plot using Matplotlib. In this tutorial, we will explore the various methods of setting camera positions for the 3D plots using Python/Matplotlib.

## Importing Libraries 
We will be using the `matplotlib`, `numpy`, `pyplot` and `mpl_toolkits.mplot3d`. You can install these libraries using the following pip command,

```python
!pip install matplotlib numpy pyplot mpl_toolkits.mplot3d
```

After installing the library, we need to import the libraries as shown below,

```python
import matplotlib.pyplot as plt
import numpy as np
from mpl_toolkits.mplot3d import Axes3D
```

## Setting Camera Positions
There are several ways to set camera positions for 3D plots. We will discuss two essential methods.

### Method 1: Using view_init() Function
The `view_init()` function sets the camera's elevation and azimuthal angles. The syntax of the `view_init()` function is given below,

```python
view_init(elev=None, azim=None)
```

Where `elev` is the elevation angle in the z plane and `azim` is the azimuthal angle in the x,y plane. 

For example, we can set the camera position using the view_init() function as follows,

```python
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.scatter(x, y, z, c='r', marker='o')
ax.view_init(elev=40, azim=-120)
```

### Method 2: Using set_axis_off() and set_axis_on() Functions

The `set_axis_off()` function removes the axis's bounding box, while the `set_axis_on()` function adds the axis bounding box. When the bounding box is removed, the plot appears flat, and it becomes easy to set the camera's position.

```python
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.scatter(x, y, z, c='r', marker='o')
ax.set_axis_off()
```

We can then set the camera's position by dragging the plot using the mouse. Once the desired position is reached, we can add the axis back using the `set_axis_on()` function. 

```python
ax.set_axis_on()
```


## Conclusion 
In conclusion, we learned two essential methods of setting camera positions for 3D plots in Python/Matplotlib. The first method used the `view_init()` function to set the camera's elevation and azimuthal angles, while the second method used the `set_axis_off()` and `set_axis_on()` functions to remove and add the axis's bounding box, respectively.
