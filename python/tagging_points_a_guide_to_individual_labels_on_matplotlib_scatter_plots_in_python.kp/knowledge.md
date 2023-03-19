---
title: What is the method for assigning individual tags to a scatter plot in matplotlib?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `scatter` function`s `label` parameter to assign a label to each point, and then call `legend` function to create individual tags for the scatter plot.
---

**Contents**

[TOC]

# Introduction

A scatter plot is a type of plot that displays the relationship between two variables. It is a great way to visualize data points in a two-dimensional plane. Matplotlib is a popular data visualization library that can create scatter plots among other types of plots. In this tutorial, we will learn how to put individual tags for a matplotlib scatter plot in Python. 

# Creating a Scatter Plot with Matplotlib

Before we can add individual tags to a scatter plot, we must first create a scatter plot using the Matplotlib library. We can do this by following the steps below:

1. Import the matplotlib library:

   ```
   import matplotlib.pyplot as plt
   ```

2. Define the x and y data:

   ```
   x = [1, 2, 3, 4, 5]
   y = [4, 3, 6, 2, 7]
   ```

3. Create the scatter plot using the `scatter` function:

   ```
   plt.scatter(x, y)
   plt.show()
   ```

   This will create a scatter plot with the x-axis representing the values in the `x` list and the y-axis representing the values in the `y` list.

# Adding Individual Tags to a Scatter Plot

Now that we have created a scatter plot, we can add individual tags to the data points. We can do this by following the steps below:

1. Define the tags we want to add to the scatter plot:

   ```
   tags = ['a', 'b', 'c', 'd', 'e']
   ```

   This defines the individual tags that we want to add to the data points.

2. Loop through the data points and add the tags using the `annotate` function:

   ```
   for i, tag in enumerate(tags):
       plt.annotate(tag, (x[i], y[i]))
   ```

   This will loop through each data point and add the corresponding tag at the same location as the data point.

3. Display the updated scatter plot:

   ```
   plt.scatter(x, y)
   for i, tag in enumerate(tags):
       plt.annotate(tag, (x[i], y[i]))
   plt.show()
   ```

   This will display the updated scatter plot with the individual tags at the data points.

# Conclusion

In this tutorial, we learned how to put individual tags for a matplotlib scatter plot in Python. We created a scatter plot using the Matplotlib library and added individual tags to the data points using the `annotate` function. This can be useful in adding labels or additional information to the data points in the scatter plot.
