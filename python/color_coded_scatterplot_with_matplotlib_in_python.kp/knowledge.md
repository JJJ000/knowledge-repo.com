---
title: A scatterplot in matplotlib that incorporates color as a representation of a third variable
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use the `c` parameter in the scatter function to specify the values of the third variable that will determine the color of the markers in the scatterplot.
---

**Contents**

[TOC]

Section 1: Introduction
Matplotlib is a popular data visualization library in Python. It provides various tools for creating static, animated, and interactive plots. One of the most common types of visualization that is used in data analysis is scatterplots. Scatterplots are used for plotting two continuous variables and can be enhanced by adding color based on a third variable. In this tutorial, we will learn how to create a scatterplot in Matplotlib and how to color the points based on a third variable.


Section 2: Creating a basic scatterplot
In Matplotlib, scatterplots can be created using the scatter function. The basic syntax for creating a scatterplot is:

```
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.scatter(x, y)
plt.show()
```

This code will create a scatterplot with x as the horizontal axis and y as the vertical axis. By default, the points will be black and without any marker. 

Section 3: Adding color to the scatterplot
To add color to the scatterplot, we need to define a third variable that represents the value of the color for each point. In the following example, we will use the numpy.random.rand function to generate random values between 0 and 1 for the color variable.

```
import numpy as np
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]
color = np.random.rand(5)

plt.scatter(x, y, c=color)
plt.show()
```

In this example, we added `c=color` to the scatter function, which tells Matplotlib to use the values in the color variable to set the color of each point. The `c` parameter can be set to a list or array of the same length as x and y.

Section 4: Choosing a color map
Matplotlib provides many color maps that can be used to customize the color scheme of the scatterplot. A color map is a mapping from a scalar value to a color. The default colormap is 'viridis'. 

To change the colormap, we can use the `cmap` parameter in the scatter function. For example, to use the 'cool' colormap, we can modify our previous code as follows:

```
import numpy as np
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]
color = np.random.rand(5)

plt.scatter(x, y, c=color, cmap='cool')
plt.colorbar()
plt.show()
```

In this example, we added the `cmap` parameter to the scatter function and set it to 'cool'. We also added `plt.colorbar()` to display a colorbar that shows the mapping between the color and the value of the third variable. 

The choice of the colormap depends on the data and the purpose of the visualization. Matplotlib provides a wide range of color maps that can be used for various types of data. Some of the commonly used colormaps are 'viridis', 'cool', 'hot', 'summer', and 'autumn'. 

We can also reverse the color map by using the `r cmap` parameter in the scatter function. For example, `cmap='cool_r'` will use the reversed 'cool' colormap. 

Conclusion:
In this tutorial, we learned how to create a scatterplot in Matplotlib and how to add color based on a third variable. We also learned how to choose a colormap and display a colorbar. Scatterplots with color are useful for visualizing the relationship between three variables and can provide insights into patterns and trends in the data.
