---
title: What are the steps to refresh a plot in matplotlib?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the `set\_data()` method of the plot object to update the data and the `draw()` method of the plot`s figure to redraw the plot.
---

**Contents**

[TOC]

### Section 1: Introduction
Matplotlib is a powerful library used for data visualization in Python. It provides a flexible way of creating graphs, charts, and other visual representations of data. Sometimes it is necessary to update a chart as new data becomes available or changes in real-time. In this tutorial, we will go over different ways of updating a plot in matplotlib.

### Section 2: Updating a Plot in Real-Time
To update a plot in real-time, we can use the `animate` function provided by matplotlib. Here are the steps to update a plot:

1. Import the `FuncAnimation` module from matplotlib.
2. Create a figure and axis for the plot.
3. Define a function that will update the data in the plot.
4. Use the `FuncAnimation` module to animate the plot.

Here is an example code snippet that updates a line plot in real-time:

```
import matplotlib.pyplot as plt
import numpy as np
from matplotlib.animation import FuncAnimation

# Create the figure and axis objects
fig, ax = plt.subplots()

# Initialize the line object
line, = ax.plot([], [])

# Define the function to update the data in the plot
def update(i):
    x = np.linspace(0, 2*np.pi, 100)
    y = np.sin(x-i/10)
    line.set_data(x, y)
    return line,

# Use the FuncAnimation module to animate the plot
ani = FuncAnimation(fig, update, frames=100, blit=True)

# Show the plot
plt.show()
```

In this example, the `update` function generates new data for the sine wave and updates the line data using the `set_data` method. The `FuncAnimation` module is used to animate the plot by calling the `update` function repeatedly.

### Section 3: Updating a Plot with New Data
Another way to update a plot is to update the data itself. Here are the steps to update a plot with new data:

1. Import the necessary modules.
2. Create a figure and axis for the plot.
3. Initialize the plot by plotting the initial data.
4. Update the data of the plot using the `set_data` method.
5. Call the `draw` method to redraw the plot.

Here is an example code snippet that updates a line plot with new data:

```
import matplotlib.pyplot as plt
import numpy as np

# Create the figure and axis objects
fig, ax = plt.subplots()

# Initialize the plot with initial data
x = np.linspace(0, 2*np.pi, 100)
y = np.sin(x)
line, = ax.plot(x, y)

# Update the plot with new data
x1 = np.linspace(0, 2*np.pi, 100)
y1 = np.sin(x1+np.pi/2)
line.set_data(x1, y1)

# Redraw the plot
ax.draw()

# Show the plot
plt.show()
```

In this example, the `set_data` method is used to update the data of the line plot, and the `draw` method is used to redraw the plot with the updated data.

### Section 4: Conclusion
In this tutorial, we have gone over different ways of updating a plot in matplotlib. We have seen how to update a plot in real-time using the `animate` function, and how to update a plot with new data using the `set_data` and `draw` methods. These techniques can be useful for displaying data in real-time or updating a plot with new data as it becomes available.
