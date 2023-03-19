---
title: What is the procedure for creating two plots adjacent to each other?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use Matplotlib`s subplots() function with the argument `nrows=1, ncols=2` to create two side-by-side plots.
---

**Contents**

[TOC]

## Section 1: Import Packages and Generate Data

To make two plots side-by-side in Python, we will need to use the following packages:
- `matplotlib`: for creating plots
- `numpy`: for generating data

Let's start by importing these two packages and generating some dummy data to plot.

```python
import matplotlib.pyplot as plt
import numpy as np

# generate data
x = np.linspace(0, 10, 100)
y1 = np.sin(x)
y2 = np.cos(x)
```

## Section 2: Create Subplots

To make two plots side-by-side, we need to create a single figure with two subplots. We can use the `plt.subplots()` function to create a figure and subplots.

```python
fig, ax = plt.subplots(nrows=1, ncols=2, figsize=(10, 5))
```

The above code creates a figure with one row and two columns of subplots, each with a size of `(10, 5)`.

We can access each subplot using the `ax` variable, which is a 2D array of the subplots. For example, to plot `y1` on the first subplot and `y2` on the second subplot, we can use:

```python
ax[0].plot(x, y1)
ax[1].plot(x, y2)
```

Notice that we use `ax[0]` and `ax[1]` to access the first and second subplots, respectively.

## Section 3: Customize Plots

Now that we have created our subplots and plotted the data, we can customize the appearance of the plots using various `plt.` functions.

For example, we can set the titles and labels of the two subplots using:

```python
ax[0].set_title("Sin(x)")
ax[1].set_title("Cos(x)")
ax[0].set_xlabel("x")
ax[1].set_xlabel("x")
ax[0].set_ylabel("y")
```

We can also add a legend to each subplot by specifying a label for each plot and using the `ax.legend()` function:

```python
ax[0].plot(x, y1, label="sin(x)")
ax[1].plot(x, y2, label="cos(x)")
ax[0].legend()
ax[1].legend()
```

Finally, we can save the figure using the `plt.savefig()` function:

```python
plt.savefig("figure.png")
```

## Section 4: Full code

Putting it all together, the full code to make two plots side-by-side in Python is:

```python
import matplotlib.pyplot as plt
import numpy as np

# generate data
x = np.linspace(0, 10, 100)
y1 = np.sin(x)
y2 = np.cos(x)

# create subplots
fig, ax = plt.subplots(nrows=1, ncols=2, figsize=(10, 5))

# plot data
ax[0].plot(x, y1, label="sin(x)")
ax[1].plot(x, y2, label="cos(x)")

# customize plots
ax[0].set_title("Sin(x)")
ax[1].set_title("Cos(x)")
ax[0].set_xlabel("x")
ax[1].set_xlabel("x")
ax[0].set_ylabel("y")
ax[1].legend()
ax[1].legend()

# save figure
plt.savefig("figure.png")
```
