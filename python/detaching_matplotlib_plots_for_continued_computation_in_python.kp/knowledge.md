---
title: Can matplotlib plots be detached to enable computation to continue?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, you can use the `plt.ion()` command in matplotlib to detach the plot and continue with computation in Python.
---

**Contents**

[TOC]

Yes, there is a way to detach matplotlib plots so that the computation can continue in Python. One way to achieve this is by using the `TkAgg` backend, which allows for non-blocking interactive figures. 

### Setting the backend to TkAgg 

The first step is to import the necessary libraries and set the backend to `TkAgg`. 

```python 
import matplotlib.pyplot as plt
plt.switch_backend('TkAgg')
```

### Creating a non-blocking plot 

To create a non-blocking plot, we can use the `ion` (interactive on) function provided by Matplotlib. This function turns on interactive mode and enables the plot to be updated as new data is added. 

```python 
plt.ion()
```

Then, we can create the plot using the standard `plot` function, and use `pause` to allow for other computations while the plot is being displayed. 

```python 
plt.plot(x, y)
plt.pause(0.01)
```

### Updating the plot 

To update the plot with new data, simply call `plot` again with the new values, and use pause to continue code execution. 

```python 
plt.plot(x_new, y_new)
plt.pause(0.01)
```

### Turning off interactive mode 

Once the plot is no longer needed, we can turn off interactive mode by calling `ioff`. 

```python 
plt.ioff()
```

With these steps, it is possible to detach Matplotlib plots and continue with other computations in Python.
