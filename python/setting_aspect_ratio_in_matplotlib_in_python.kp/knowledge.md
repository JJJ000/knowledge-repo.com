---
title: What is the method to set the aspect ratio in matplotlib?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: The aspect ratio in Matplotlib can be set using the aspect parameter in the plt.subplots() or plt.figure() functions.
---

**Contents**

[TOC]

Setting Aspect Ratios in Matplotlib

In Matplotlib, it is possible to set the aspect ratio of a figure, axis, or subplot. The aspect ratio is the ratio of the height to the width of a figure or axis. By setting the aspect ratio, it is possible to control the shape of a figure or axis and ensure that the plot is not distorted.

In this tutorial, we will explain how to set the aspect ratio in Matplotlib in Python.

1. Setting the Aspect Ratio of a Figure

To set the aspect ratio of a figure in Matplotlib, we can use the `figure()` function's `figaspect` parameter. This parameter takes a tuple of two values, which represent the width and height of the figure in inches. The aspect ratio is calculated as the ratio of the height to the width.

``` python
import matplotlib.pyplot as plt

fig_width = 6.0
fig_height = 4.0
fig = plt.figure(figaspect=(fig_width/fig_height))
```

In this example, we set the width of the figure to 6 inches and the height to 4 inches. The aspect ratio is calculated as 4/6=0.67. The resulting figure will have a height-to-width aspect ratio of 0.67.

2. Setting the Aspect Ratio of an Axis

To set the aspect ratio of an axis in Matplotlib, we can use the `set_aspect` method of the `Axes` class. This method takes a string or a float as a parameter.

``` python
fig, ax = plt.subplots()
ax.set_aspect('equal')
```

In this example, we create a new figure and a new axis object. We then call the `set_aspect` method and pass the string `'equal'` as a parameter. This ensures that the axis has an equal aspect ratio, meaning that the height and width of the plot are proportional.

Alternatively, we can pass a float value as a parameter to set the aspect ratio to a specific value.

``` python
fig, ax = plt.subplots()
ax.set_aspect(2.0)
```

In this example, we set the aspect ratio to 2.0, meaning that the height of the plot will be twice as long as the width.

3. Setting the Aspect Ratio of a Subplot

To set the aspect ratio of a subplot in Matplotlib, we can use the same approach as setting the aspect ratio of an axis. We can call the `set_aspect` method of the `Axes` class for each subplot.

``` python
fig, axs = plt.subplots(2, 2)
for ax in axs.flat:
    ax.set_aspect('equal')
```

In this example, we create a figure with a 2x2 grid of subplots. We then loop over each subplot and call the `set_aspect` method with the string `'equal'` as a parameter. This ensures that each subplot has an equal aspect ratio.

4. Conclusion

In this tutorial, we have explained how to set the aspect ratio in Matplotlib in Python. We have shown how to set the aspect ratio of a figure, axis, and subplot using the `figure()`, `set_aspect`, and `subplots` functions, respectively. By setting the aspect ratio, we can control the shape of a plot and ensure that the plot is not distorted.
