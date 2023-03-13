---
title: What is the process of configuring the upper limit as 'auto', while maintaining a static lower limit using matplotlib.pyplot?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the pyplot.ylim() function with the lower limit value as the first argument and None as the second argument.
---

**Contents**

[TOC]

## Introduction

Matplotlib's `pyplot` module provides several functions for plotting graphs in Python. In some cases, auto-scaling the upper limit for the y-axis might be necessary while keeping the lower limit fixed. This tutorial shows how to achieve this using `pyplot` module in Matplotlib.

## Step 1: Importing necessary modules

Before we can start plotting, we need to import the necessary modules. In this case, we will be using `matplotlib.pyplot`. 

```python
import matplotlib.pyplot as plt
```

## Step 2: Creating sample data 

For the purpose of this tutorial, let us create some sample data that we can plot.

```python
import numpy as np

x = np.arange(0, 10, 0.1)
y = np.sin(x)
```

We are using `numpy` module to create `x` and `y` variables.

## Step 3: Setting up the plot

We can now create a new figure and set up our axis labels and title.

```python
fig, ax = plt.subplots()

ax.set_xlabel("x values")
ax.set_ylabel("y values")
ax.set_title("Sample graph")
```

## Step 4: Setting a fixed lower limit and auto upper limit

Finally, we can plot our data and set the y-axis limits. We will set a fixed lower limit of -1 for y-axis and let matplotlib automatically choose the upper limit.

```python
ax.plot(x, y)

ax.set_ylim(-1, None)

plt.show()
```

Here, we use `None` as the upper limit, which tells matplotlib to automatically choose the upper limit. We set `-1` as the lower limit, which remains fixed.

## Conclusion

In this tutorial, we have learned how to set the y-axis limits in matplotlib.pyplot. We have specifically looked at how to set a fixed lower limit and an auto upper limit.
