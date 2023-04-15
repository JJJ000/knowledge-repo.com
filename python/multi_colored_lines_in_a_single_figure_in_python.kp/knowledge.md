---
title: What is the method to obtain variously colored lines for individual plots in a sole illustration?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Specify the color parameter in the plot function for each plot to set different colors for each line in the same figure.
---

**Contents**

[TOC]

Section 1: Importing necessary libraries

To plot different colored lines for different plots in a single figure in Python, we need to import the necessary libraries. The commonly used libraries are `numpy` and `matplotlib`.

```python
import numpy as np
import matplotlib.pyplot as plt
```

Section 2: Plotting multiple lines with different colors in a single figure

To plot different colored lines for different plots in a single figure, we can use the `plot()` function of matplotlib. In this example code snippet, we plot three different lines with different colors in a single figure.

```python
x = np.array([1, 2, 3, 4, 5])
y1 = x ** 2
y2 = 2 * x
y3 = x ** 3

plt.plot(x, y1, color='red', label='y=x^2')
plt.plot(x, y2, color='blue', label='y=2x')
plt.plot(x, y3, color='green', label='y=x^3')

plt.legend()
plt.show()
```

In the `plot()` function, we first specify the x and y values for each line. Then we specify the color of each line using the `color` parameter. We can also specify a label for each line using the `label` parameter. Finally, we call the `legend()` function to show the labels and call the `show()` function to display the plot.

Section 3: Customizing the line styles and markers

We can also customize the line styles and markers for each line using the `linestyle` and `marker` parameters in the `plot()` function.

```python
x = np.array([1, 2, 3, 4, 5])
y1 = x ** 2
y2 = 2 * x
y3 = x ** 3

plt.plot(x, y1, color='red', label='y=x^2', linestyle='dashed', linewidth=2, marker='o')
plt.plot(x, y2, color='blue', label='y=2x', linewidth=2, marker='s')
plt.plot(x, y3, color='green', label='y=x^3', linestyle='dotted', linewidth=2, marker='*')

plt.legend()
plt.show()
```

Here, we have specified the line styles for each line using the `linestyle` parameter. We have also specified the markers for each line using the `marker` parameter.

Section 4: Using a color map to plot multiple lines

We can also use a color map to plot multiple lines with different colors in a single figure. The `cm` module in matplotlib provides a variety of color maps that we can use.

```python
x = np.linspace(0, 10, 100)
ys = np.linspace(1, 5, 4).reshape(-1, 1)
colors = plt.cm.rainbow(np.linspace(0, 1, ys.shape[0]))

for i, c in enumerate(colors):
    y = np.sin(x) * ys[i]
    plt.plot(x, y, color=c, label='y=sin(x)*{}'.format(ys[i][0]))

plt.legend()
plt.show()
```

Here, we have used the `linspace()` function to generate different y values and reshape them into a 2D array. We have also used the `cm.rainbow()` function to generate a range of colors from the rainbow color map. Then, we have plotted each line using a loop and specified the color of each line using the corresponding color from the color map.
