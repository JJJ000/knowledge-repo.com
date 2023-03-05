---
title: What is the process for configuring the axis range in subplot?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the `set\_xlim` and `set\_ylim` methods on the subplot object to set the range of the x and y axis, respectively.
---

**Contents**

[TOC]

## Introduction

Matplotlib is a popular data visualization library in Python. It is highly customizable and can be used to create a wide range of plots, from simple line graphs to complex 3D visualizations. In this tutorial, we will explore how to set the subplot axis range in Python using Matplotlib.

## Prerequisites

To follow this tutorial, you will need:

- Python 3.x installed on your computer
- Matplotlib installed on your computer

## Creating a Figure and Subplots

To set the subplot axis range in Python, we must first create a figure and subplots using Matplotlib. The figure is the top-level container for all the plot elements, while the subplots are the individual plots that make up the figure. 

```python
import matplotlib.pyplot as plt

fig, axs = plt.subplots(nrows=2, ncols=2, figsize=(8, 6))
```

Here, we are creating a 2x2 grid of subplots with a figure size of 8x6 inches. The `subplots` function returns two arrays: one for the figure and one for the subplots themselves. 

## Changing the Axis Range

Once the subplots have been created, we can adjust the axis range using the `set_xlim` and `set_ylim` methods. These methods allow us to set the minimum and maximum values for the x and y axes, respectively. 

```python
axs[0, 0].set_xlim([0, 10])
axs[0, 0].set_ylim([0, 20])
```

Here, we are setting the x-axis range to be between 0 and 10 and the y-axis range to be between 0 and 20 for the top-left subplot. Note that we are selecting the subplot using the `axs` array and the indexing convention of `[row, column]`.

## Conclusion

In this tutorial, we have explored how to set the subplot axis range in Python using Matplotlib. By creating a figure and subplots and then adjusting the axis range with the `set_xlim` and `set_ylim` methods, we can customize our plots to better suit our needs.
