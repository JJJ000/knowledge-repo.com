---
title: Convert the y axis to a percentage format
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Set the y-axis to display as percent using the `PercentFormatter` function from the matplotlib.ticker library in Python.
---

**Contents**

[TOC]

## Section 1: Introduction
In Python, the `matplotlib` library is used to create visualizations such as charts and graphs. When creating these visualizations, it is often useful to format the y-axis as a percentage. 

## Section 2: Code for formatting y-axis as percent 
The following code can be used to format the y-axis as a percentage in Python:

```python
import matplotlib.pyplot as plt
from matplotlib.ticker import PercentFormatter

# create sample data
x = [1, 2, 3, 4]
y = [0.1, 0.25, 0.5, 0.75]

# create plot
fig, ax = plt.subplots()

# set y-axis formatter to percent
ax.yaxis.set_major_formatter(PercentFormatter(xmax=1))

#plot data
ax.plot(x, y)

#show plot
plt.show()
```

## Section 3: Explanation of code
The `PercentFormatter` is a class from the `matplotlib.ticker` module that is used to format the y-axis as a percentage. The `xmax` parameter is set to `1` to indicate that the y-axis should display values as percentages relative to 1 (i.e., 0.1 = 10%, 0.25 = 25%, etc.). 

The `yaxis` object is used to access the y-axis of the plot, and the `set_major_formatter` method is used to apply the `PercentFormatter` to this axis. 

## Section 4: Conclusion
By using the `PercentFormatter` class in the `matplotlib` library, it is possible to format the y-axis of a visualization as a percentage in Python. This is useful for displaying data with percentages, such as in financial data or demographic information.
