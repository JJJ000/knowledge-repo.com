---
title: Minimize the margins on both the left and the right of the matplotlib plot
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To reduce left and right margins in a matplotlib plot in Python, use the `subplots\_adjust()` function with the `left` and `right` parameters.
---

**Contents**

[TOC]

## Importing necessary libraries
To reduce the left and right margins in matplotlib plot in Python, we need to import the necessary libraries first.

```python
import matplotlib.pyplot as plt
import numpy as np
```


## Setting up sample data
Let's create some sample data to plot the graph.

```python
x = np.linspace(0, 10, 100)
y = np.sin(x)
```


## Reducing left and right margins
Now, we can reduce the left and right margins by setting the `subplots_adjust` parameter in matplotlib with the `left` and `right` parameters.

```python
plt.subplots_adjust(left=0.05, right=0.98)
plt.plot(x, y)
plt.show()
```


## Visualizing the plot
After running these pieces of code, we can now see the plot with reduced left and right margins. 

![Reduced left and right margin plot](https://i.imgur.com/XhzvvgU.png)
