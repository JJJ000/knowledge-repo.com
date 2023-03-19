---
title: How to generate distinct line styles for major and minor gridlines in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Use the methods `set\_major\_gridlines` and `set\_minor\_gridlines` with the `linestyle` parameter set to the desired line style.
---

**Contents**

[TOC]

## Section 1: Importing Required Libraries

To create major and minor gridlines with different linestyles in Python, we need to use the Matplotlib library, which is a popular data visualization library. We will also need the `pyplot` module from Matplotlib to create the plot and set its properties, and the `ticker` module to set the tick locations and labels.

```python
import matplotlib.pyplot as plt
import matplotlib.ticker as ticker
```

## Section 2: Creating the Plot

Next, we need to create the plot itself. We can use the `plot` function from `pyplot` to plot our data, and then use the `grid` function to add the gridlines to the plot. By default, both major and minor gridlines have the same linestyle, which is a solid line. To create different linestyles for major and minor gridlines, we need to set the `linestyle` property of the `x` and `y` gridlines separately.

```python
# Create the plot
plt.plot(x_data, y_data)

# Set the gridlines
plt.grid(True, which='both')

# Set the major and minor gridline styles
plt.gca().xaxis.grid(True, linestyle='--', which='major', color='lightgrey')
plt.gca().xaxis.grid(True, linestyle=':', which='minor', color='lightgrey')
plt.gca().yaxis.grid(True, linestyle='--', which='major', color='lightgrey')
plt.gca().yaxis.grid(True, linestyle=':', which='minor', color='lightgrey')

# Show the plot
plt.show()
```

## Section 3: Setting the Tick Locations and Labels

To make our plot more readable, we can also set the tick locations and labels using the `ticker` module. We can use the `MultipleLocator` class from the `ticker` module to set the tick locations, and the `FormatStrFormatter` class to set the tick labels.

```python
# Set the tick locations and labels
plt.gca().xaxis.set_major_locator(ticker.MultipleLocator(10))
plt.gca().xaxis.set_minor_locator(ticker.MultipleLocator(2))
plt.gca().yaxis.set_major_locator(ticker.MultipleLocator(0.5))
plt.gca().yaxis.set_minor_locator(ticker.MultipleLocator(0.1))
plt.gca().xaxis.set_major_formatter(ticker.FormatStrFormatter('%d'))
plt.gca().yaxis.set_major_formatter(ticker.FormatStrFormatter('%.1f'))
```

## Section 4: Finalizing the Plot

Finally, we can customize the plot further by adding a title, axes labels, and legend. We can use the `title`, `xlabel`, `ylabel`, and `legend` functions from the `pyplot` module to set these properties.

```python
# Add title and axes labels
plt.title('My Plot')
plt.xlabel('X-Axis Label')
plt.ylabel('Y-Axis Label')

# Add legend
plt.legend(['Data'])

# Show the plot
plt.show()
```

By using these techniques, we can create visually appealing plots with major and minor gridlines of different linestyles in Python.
