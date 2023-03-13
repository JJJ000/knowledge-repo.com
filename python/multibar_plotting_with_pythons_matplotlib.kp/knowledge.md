---
title: Generating multiple bars using python's matplotlib
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To create multiple bars in matplotlib in Python, you can use the `bar` function multiple times within a single figure or subplot.
---

**Contents**

[TOC]

## Introduction
Matplotlib is a powerful visualization library in Python that offers a wide range of tools for creating different types of charts, including bar charts. With Matplotlib, it's possible to create multiple bars in the same bar chart easily. In this article, we will explore how to create multiple bars in Python Matplotlib.

## Data Preparation
Before we proceed, we need to prepare data for multiple bars. For instance, if we want to create a bar chart that shows the number of apples, bananas, and oranges sold in a store, we need to have data on the number of each fruit sold. We can create a dictionary with each fruit as a key and its corresponding value as the number of fruits sold, as shown below.

```python
data = {"apples": [20, 25, 30], "bananas": [10, 15, 20], "oranges": [15, 30, 25]}
```

The above dictionary shows the number of apples, bananas, and oranges sold over three days.

## Creating Multiple Bars
To create multiple bars for each fruit, we can use the `plt.bar()` function of Matplotlib. We can loop through each fruit in the `data` dictionary and draw a bar chart for each fruit. The code below demonstrates how we can create multiple bars in Matplotlib.

```python
import matplotlib.pyplot as plt

data = {"apples": [20, 25, 30], "bananas": [10, 15, 20], "oranges": [15, 30, 25]}

# Set the x-axis labels
labels = ["Day 1", "Day 2", "Day 3"]

# Loop through each fruit and plot the bar chart
for i, (fruit, values) in enumerate(data.items()):
    plt.bar([x + i*0.2 for x in range(len(values))], values, width=0.2, label=fruit)

# Set the x-axis tick marks
plt.xticks([0.2, 1.2, 2.2], labels)

# Add the legend
plt.legend()

# Show the plot
plt.show()
```

In the above code, we loop through each fruit in the `data` dictionary using the `.items()` method. We then use the `plt.bar()` function to plot the bar chart for each fruit. We use the `enumerate()` function to assign a unique index `i` to each fruit, which we use to move the bars slightly away from each other for better visualization.

We also set the `width` of each bar to 0.2 to leave some distance between each fruit. The `label` parameter allows us to add a legend to the plot.

Finally, we set the `xticks` to the days for which we have sales data, add the legend, and show the plot using the `plt.show()` function.

## Conclusion
In this article, we explored how to create multiple bars in a bar chart using Python Matplotlib. We demonstrated how to prepare data, plot multiple bars using a loop, and customize the plot to make it more readable. By following these steps, you can create stunning visualizations in Python Matplotlib with multiple bars.
