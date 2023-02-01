---
title: Change the orientation of axis labels in Python matplotlib
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: You can rotate axis text in matplotlib by setting the rotation parameter of the set\_xticklabels or set\_yticklabels methods.
---

**Contents**

[TOC]

1. Setting the Rotation Angle 

To rotate the axis text in Python Matplotlib, use the `set_rotation()` function. This function takes a numeric argument which represents the angle of rotation. 

2. Setting the Horizontal Alignment 

The `set_rotation()` function also allows you to set the horizontal alignment of the axis text. This is done by passing in a string argument, which can be either ‘left’, ‘center’ or ‘right’. 

3. Setting the Vertical Alignment 

The `set_rotation()` function also allows you to set the vertical alignment of the axis text. This is done by passing in a string argument, which can be either ‘top’, ‘center’ or ‘bottom’. 

4. Example Code 

The following example code demonstrates how to use the `set_rotation()` function to rotate the axis text in Python Matplotlib. 

```
# import matplotlib
import matplotlib.pyplot as plt

# create a figure
fig = plt.figure()

# create an axis
ax = fig.add_subplot(111)

# set the rotation angle
ax.set_rotation(45)

# set the horizontal alignment
ax.set_rotation('left')

# set the vertical alignment
ax.set_rotation('top')

# show the figure
plt.show()
```
