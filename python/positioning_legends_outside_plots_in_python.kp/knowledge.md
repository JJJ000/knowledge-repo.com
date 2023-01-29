---
title: How can the legend be placed outside the plot?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To put the legend outside the plot in Python, use the `bbox\_to\_anchor` parameter in the `legend()` function.
---

**Contents**

[TOC]

# Section 1: Setting the Legend Outside the Plot

In Python, setting the legend outside the plot can be done using the `plt.legend()` function. This function takes the argument `loc` which can be used to specify the location of the legend outside the plot.

# Section 2: Specifying the Location of the Legend

The `loc` argument of the `plt.legend()` function can take a string, an integer, or a pair of floats. 

- If a string is used, it should be one of the following: ‘best’, ‘upper right’, ‘upper left’, ‘lower left’, ‘lower right’, ‘right’, ‘center left’, ‘center right’, ‘lower center’, ‘upper center’, or ‘center’.

- If an integer is used, it should be a value between 0 and 10.

- If a pair of floats is used, it should be a tuple of two values which specify the x and y coordinates of the legend in the figure coordinate system.

# Section 3: Example

Here is an example of setting the legend outside the plot in Python:

```
import matplotlib.pyplot as plt

# Create a figure and an axes
fig, ax = plt.subplots()

# Plot some data
ax.plot(x, y, label='Data')

# Set the legend outside the plot
plt.legend(loc='upper left')
```

# Section 4: Additional Arguments

In addition to the `loc` argument, the `plt.legend()` function takes several other arguments which can be used to customize the legend. These arguments include `bbox_to_anchor`, `ncol`, `frameon`, `shadow`, and `fancybox`. For more information on these arguments, please refer to the official documentation.
