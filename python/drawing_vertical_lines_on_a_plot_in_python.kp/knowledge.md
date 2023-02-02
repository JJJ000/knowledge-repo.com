---
title: What is the procedure for adding vertical lines to a plot?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: To draw vertical lines on a given plot in Python, use the Axes.axvline() method.
---

**Contents**

[TOC]

## Step 1: Import Libraries 

The first step is to import the necessary libraries. The most common library used for plotting in Python is `matplotlib`.

```
import matplotlib.pyplot as plt
```

## Step 2: Create a Plot

The next step is to create a plot. This can be done using the `plt.plot()` function. For example, to create a simple line plot:

```
x = [1, 2, 3, 4, 5]
y = [1, 4, 9, 16, 25]

plt.plot(x, y)
```

## Step 3: Add Vertical Lines

The third step is to add vertical lines to the plot. This can be done using the `plt.vlines()` function. For example, to add a vertical line at x = 2.5:

```
plt.vlines(2.5, 0, 25)
```

## Step 4: Show the Plot

The final step is to show the plot. This can be done using the `plt.show()` function.

```
plt.show()
```
