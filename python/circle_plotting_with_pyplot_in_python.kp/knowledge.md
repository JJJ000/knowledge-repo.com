---
title: Create a circle using pyplot
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To plot a circle with pyplot in Python, use the `circle` function from the `matplotlib.patches` module with the desired circle coordinates and radius.
---

**Contents**

[TOC]

## Installing required modules

First, we need to install the required modules. We will use `pyplot` module from `matplotlib`. We can install it from the command line using pip. Run the following command to install `matplotlib`:

```
pip install matplotlib
```

If you are using Jupyter Notebook, you can install the module by adding ! before the command. Run the following code in a new cell:
```python
!pip install matplotlib
``` 


## Importing modules

After installing the `matplotlib` package, we need to import it in our python code. We will use the `pyplot` module from `matplotlib` to plot the circle. 

```python
import matplotlib.pyplot as plt
```

## Plotting a circle

To plot a circle with `pyplot`, we can use the `Circle` function from `matplotlib.patches` module. 

```python
from matplotlib.patches import Circle

fig, ax = plt.subplots()

circle = Circle(xy=(0, 0), radius=1.0, fill=False)
ax.add_patch(circle)

plt.show()
```

Here, we create a new `Figure` and a new set of `Axes` using the `subplots()` function from the `pyplot` module. Then, we use the `Circle` function from the `matplotlib.patches` module to create a new circle. The `xy` parameter defines the center of the circle, and the `radius` parameter defines the radius of the circle. We set the `fill` parameter to `False` to make an unfilled circle. Finally, we add the created circle to the `Axes` object using the `add_patch()` method, and use the `show()` function from the `pyplot` module to show the plot. 

The resulting plot will be a circle centered at the origin with a radius of 1.0.
