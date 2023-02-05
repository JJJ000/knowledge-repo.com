---
title: A plot showing the relationship between two variables, with a different label or text accompanying each data point
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: A scatter plot with different text at each data point can be created using the matplotlib.pyplot.text() function.
---

**Contents**

[TOC]

## Scatter Plot
A scatter plot is a type of plot that shows the relationship between two variables. It is usually used to illustrate the correlation between two variables. A scatter plot can be created using the `matplotlib.pyplot.scatter()` function.

## Adding Text
To add text at each data point, the `matplotlib.pyplot.text()` function can be used. This function takes in the x and y coordinates of the data point, as well as the text to be displayed.

## Setting Text Properties
The text properties can be set using the `matplotlib.pyplot.text()` function. This includes the font size, color, and rotation of the text.

## Example
The following is an example of a scatter plot with different text at each data point.

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4]
y = [4, 3, 2, 1]

plt.scatter(x, y)

plt.text(1, 4, 'A', fontsize=20, color='green', rotation=45)
plt.text(2, 3, 'B', fontsize=20, color='red', rotation=45)
plt.text(3, 2, 'C', fontsize=20, color='blue', rotation=45)
plt.text(4, 1, 'D', fontsize=20, color='orange', rotation=45)

plt.show()
```
