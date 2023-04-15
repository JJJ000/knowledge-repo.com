---
title: How can I balance the scales of both the x-axis and y-axis?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the aspect ratio option in matplotlib to equalize the scales of the x-axis and y-axis.
---

**Contents**

[TOC]

# Introduction
When it comes to data visualization, having properly scaled axes is essential. In this tutorial, we will go over how to equalize the scales of both the x-axis and y-axis in Python.

# Step 1: Import the necessary libraries
We will be using the `matplotlib` library to create our plots. Therefore, it needs to be imported into our Python script. To do that, we use the following code:

```python
import matplotlib.pyplot as plt
```

# Step 2: Create a scatter plot
In this tutorial, we will be using a scatter plot to show how to equalize the scales of both the x-axis and y-axis. Let's create a scatter plot using `matplotlib`:

```python
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.scatter(x, y)
plt.show()
```

This code will produce a scatter plot with our data points. However, the x-axis and y-axis scales are not equal.

# Step 3: Equalize the scales of the x-axis and y-axis
To equalize the scales of both the x-axis and y-axis, we can use the `plt.axis('equal')` function. This function takes no arguments and sets the x-axis and y-axis scales to be the same. Here's what it looks like in our example:

```python
plt.scatter(x, y)
plt.axis('equal')
plt.show()
```

This code will produce a scatter plot with the x-axis and y-axis scales equalized.

# Step 4: Final code
Here's the final code that creates the scatter plot and equalizes the scales of the x-axis and y-axis:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.scatter(x, y)
plt.axis('equal')
plt.show()
```

This code will produce a scatter plot with the x-axis and y-axis scales equalized.
