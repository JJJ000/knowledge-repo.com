---
title: Plot a graph with logarithmic scales on the axes
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: To plot logarithmic axes in Python, use the plt.xscale() and plt.yscale() functions with the `log` argument.
---

**Contents**

[TOC]

**Section 1: Setting Up the Logarithmic Axes**

The first step in plotting logarithmic axes in Python is to import the necessary libraries. For this example, we will use the `matplotlib` library.

```python
import matplotlib.pyplot as plt
```

Next, create a figure and set the x- and y-axes to be logarithmic.

```python
fig, ax = plt.subplots()
ax.set_xscale('log')
ax.set_yscale('log')
```

**Section 2: Plotting Data**

Now that the axes are set up, we can plot some data. For example, let’s plot some x and y values.

```python
x = [1, 10, 100, 1000]
y = [1, 10, 100, 1000]

ax.plot(x, y)
```

**Section 3: Customizing the Axes**

We can also customize the axes. For example, let’s set the x-axis and y-axis limits.

```python
ax.set_xlim(1, 1000)
ax.set_ylim(1, 1000)
```

We can also add labels to the axes.

```python
ax.set_xlabel('x')
ax.set_ylabel('y')
```

**Section 4: Showing the Plot**

Finally, we can show the plot.

```python
plt.show()
```
