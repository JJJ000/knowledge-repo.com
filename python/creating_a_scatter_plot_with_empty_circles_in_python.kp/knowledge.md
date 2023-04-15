---
title: What is the process for creating a scatter plot with unfilled circles using python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To make a scatter plot with empty circles in Python, use the marker parameter in the scatter function and set it to `o`.
---

**Contents**

[TOC]

Section 1: Introduction
Scatter plots are used to visually represent data points with two or more variables. Python provides a wide variety of libraries to create these plots, including Matplotlib and Seaborn. To create an empty circle scatter plot in Python, we will be using the Matplotlib library.

Section 2: Code
Here is the code to create an empty circle scatter plot in Python using Matplotlib:

```python
import matplotlib.pyplot as plt

# sample data
x = [1, 2, 3, 4, 5]
y = [10, 20, 30, 40, 50]

# creating a scatter plot with empty circles
fig, ax = plt.subplots()
ax.scatter(x, y, facecolors='none', edgecolors='r')
plt.show()
```

In this code, we first import the Matplotlib library. Next, we create two lists x and y with some sample data. Then, we create a scatter plot using the `ax.scatter()` method. 

The first argument to `ax.scatter()` is the data for the x-axis, and the second argument is the data for the y-axis. By default, the plot will have filled circles. We can make the circles empty by setting the 'facecolors' argument to 'none'.

Finally, we call the `plt.show()` method to display the plot.

Section 3: Explanation
The scatter plot in the code consists of five data points. By providing these data points, we create a blank figure and add a single subplot to it. For the scatter plot, we set the face color to none with the `facecolors` attribute and set the edge color to red with the `edgecolors` attribute.

Next, the `plt.show()` method shows the plot with the specified characteristics.

Section 4: Conclusion
In conclusion, we can use the `ax.scatter()` method of the Matplotlib library to create a scatter plot with empty circles. We can specify the empty circle option by setting the "facecolors" attribute of the scatter method to "none". This way, we can visualize our data in a way that best suits our needs.
