---
title: Rearrange the words to form a different sentence 
"draw grid lines behind other graph elements in matplotlib."
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Set the `zorder` parameter to a negative value in the `grid()` function to draw the grid lines behind other graph elements.
---

**Contents**

[TOC]

## Section 1: Setting up the Plot

To draw grid lines behind other graph elements, we first need to set up the plot using Matplotlib. We can do this by importing the `pyplot` module and creating a figure and axis object using the `subplots` function.

```python
import matplotlib.pyplot as plt

fig, ax = plt.subplots()
```

Once we have the `ax` object, we can use it to customize the plot further.


## Section 2: Adding Grid Lines

To add grid lines to the plot, we can use the `grid` method of the `ax` object. By default, the `grid` method adds grid lines on top of other graph elements, but we can change this behavior by setting the `zorder` parameter to a negative value.

```python
ax.grid(True, zorder=-1)
```

Here, we set the first argument to `True` to enable grid lines and the `zorder` parameter to `-1` to draw the grid lines behind other graph elements.


## Section 3: Adding Graph Elements

After adding grid lines to the plot, we can add other graph elements such as lines, markers, and labels. These elements will automatically be displayed on top of the grid lines, as they have a higher `zorder` value by default.

```python
x = [1, 2, 3, 4, 5]
y = [1, 4, 9, 16, 25]
ax.plot(x, y)
ax.set_xlabel('x')
ax.set_ylabel('y')
ax.set_title('Grid lines behind graph elements')
```

Here, we first define some data points for `x` and `y`, and then plot them using the `plot` method of the `ax` object. We also add labels for the x- and y-axes and a title for the plot.


## Section 4: Displaying the Plot

Finally, we can display the plot using the `show` method of the `pyplot` module.

```python
plt.show()
```

This will open a window displaying the plot with grid lines behind other graph elements.
