---
title: How to position text in the top left corner of a matplotlib plot?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `text()` function with the parameters `x=0` and `y=1` to set the text in the top left corner of the plot.
---

**Contents**

[TOC]

Section 1: Import necessary libraries and create a sample plot
```
import matplotlib.pyplot as plt
import numpy as np

# Create sample plot
x = np.arange(10)
y = x ** 2
fig, ax = plt.subplots()
ax.plot(x, y)
```

Section 2: Add text to the plot using `ax.text()`
```
# Add text to top left corner
ax.text(0.05, 0.95, 'Top left', transform=ax.transAxes, ha='left', va='top')
```
Explanation: `ax.text()` adds text to the given axes (`ax`) using the transform `ax.transAxes` so that the text is positioned relative to the axes. The text is aligned to the left (`ha='left'`) and top (`va='top'`) of the given coordinates `(0.05, 0.95)` that specify the position relative to the top left corner of the axes.


Section 3: Update font and size of the text
```
# Add text to top left corner
ax.text(0.05, 0.95, 'Top left', transform=ax.transAxes, ha='left', va='top',
        fontweight='bold', fontsize=14)
```
Explanation: The `fontweight` parameter specifies the weight of the font (e.g. 'bold') and the `fontsize` parameter specifies the size of the font in points.

Section 4: Show the plot
```
plt.show()
```
Explanation: The `plt.show()` function displays the plot on the screen.
