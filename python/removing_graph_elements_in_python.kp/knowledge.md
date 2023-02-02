---
title: What is the procedure for eliminating axes, legends, and white margins?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the `plt.axis(`off`)`, `plt.legend().set\_visible(False)`, and `plt.tight\_layout()` commands.
---

**Contents**

[TOC]

### Removing Axis

To remove an axis from a plot in Python, use the `.axes.get_xaxis().set_visible(False)` and `.axes.get_yaxis().set_visible(False)` methods. For example:

```python
import matplotlib.pyplot as plt

# Plot data
plt.plot([1,2,3,4])

# Remove the x and y axes
plt.axes.get_xaxis().set_visible(False)
plt.axes.get_yaxis().set_visible(False)

# Show the plot
plt.show()
```

### Removing Legends

To remove a legend from a plot in Python, use the `.legend().set_visible(False)` method. For example:

```python
import matplotlib.pyplot as plt

# Plot data
plt.plot([1,2,3,4], label="Data")

# Add a legend
plt.legend()

# Remove the legend
plt.legend().set_visible(False)

# Show the plot
plt.show()
```

### Removing White Padding

To remove white padding from a plot in Python, use the `plt.tight_layout()` method. For example:

```python
import matplotlib.pyplot as plt

# Plot data
plt.plot([1,2,3,4])

# Remove white padding
plt.tight_layout()

# Show the plot
plt.show()
```
