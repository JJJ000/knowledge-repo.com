---
title: What are the steps to modify the color of the axis, ticks, and labels in a plot?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Set the color parameter for the axes, ticks, and labels using the plt.tick\_params() and plt.xlabel()/plt.ylabel() functions in matplotlib.
---

**Contents**

[TOC]

## Introduction

Plots are an essential way to visualize data in a visually appealing and informative way. Python provides several libraries for plotting, including Matplotlib, which is one of the most widely used visualization libraries in the Python community. One crucial aspect of generating meaningful visuals is to customize the different elements of the plot to convey the intended message. One such customization is changing the color of the axis, ticks, and labels, which we will look at in this article.

## Changing the Color of the Axis

The axis is a standard component of any 2D or 3D plot, and customizing its appearance can improve its aesthetics and readability. To change the color of the axis, we will first import the Matplotlib library and create a sample plot.

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(-10, 10, 100)
y = x ** 2

plt.plot(x, y)
plt.show()
```

The above code will create a simple parabolic plot. To change the color of the x and y-axis, we can use the `set_color` method. 

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(-10, 10, 100)
y = x ** 2

plt.plot(x, y)
ax = plt.gca() # get current axis

ax.spines['left'].set_color('red')
ax.spines['bottom'].set_color('blue')

plt.show()
```

In the above code, we get the current axis object using the `gca()` method and then use the `set_color` method to change the color of the left and bottom axis to red and blue, respectively.

## Changing the Color of the Ticks

Ticks are the predefined values marked on the axis, representing the scale of the graph. We can customize the color of the ticks using the `tick_params` method.

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(-10, 10, 100)
y = x ** 2

plt.plot(x, y)
ax = plt.gca() # get current axis

ax.spines['left'].set_color('red')
ax.spines['bottom'].set_color('blue')

ax.tick_params(axis='both', which='major', colors='green')

plt.show()
```

In the above code, we use the `tick_params` method and specify the `axis` argument as both to apply the changes to both x and y-axis ticks. We set the `which` argument to major, meaning that we want to apply the changes to major ticks only. Finally, we set the `colors` parameter to green, which will change the color of the x and y-axis major ticks to green.

## Changing the Color of the Labels

The plot labels are essential to provide context to the plot and the data. You can customize the color of the labels using the `set_color` method.

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(-10, 10, 100)
y = x ** 2

plt.plot(x, y)
ax = plt.gca() # get current axis

ax.spines['left'].set_color('red')
ax.spines['bottom'].set_color('blue')

ax.tick_params(axis='both', which='major', colors='green')

plt.xlabel('X-axis label', color='purple')
plt.ylabel('Y-axis label', color='purple')

plt.show()
```

In the above code, we use the `xlabel` and `ylabel` methods to set the x and y-axis labels, respectively. We specify the `color` argument as purple in both cases, and this will change the color of the x and y-axis labels to purple.

## Conclusion

In this article, we looked at how to change the color of the axis, ticks, and labels for a plot in Python using Matplotlib. All of these changes are customizable to suit your needs, and the code examples provided above should give you a good starting point.
