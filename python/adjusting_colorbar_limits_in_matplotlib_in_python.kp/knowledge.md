---
title: Change the color range in matplotlib's colorbar
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To set the range of a colorbar in matplotlib in Python, use the set\_clim() method of the colorbar object.
---

**Contents**

[TOC]

## Introduction
The colorbar is an essential part of data visualization, allowing us to visually represent numerical values through color gradients. Sometimes, we would like to specify the range of values included in the colorbar, rather than allow it to be automatically determined by the data. In this guide, we will discuss different methods to set the colorbar range in Matplotlib in Python.

## Method 1: Using vmin and vmax parameters
One way to set the range of values included in a colorbar is by setting the `vmin` (minimum value) and `vmax` (maximum value) parameters when creating the plot. When data values fall outside of this range, they will be clipped to the respective vmin or vmax values.

``` python
import matplotlib.pyplot as plt
import numpy as np

data = np.random.rand(5,5) * 10

plt.imshow(data, cmap='viridis', vmin=2, vmax=8)
plt.colorbar()
plt.show()
```

In this example, the `vmin` and `vmax` values are set to 2 and 8, respectively. Note that the colorbar only includes colors within this range.

## Method 2: Using set_clim() method
Another way to set the colorbar range is by using the `set_clim()` method on the plotted image. This method takes in the vmin and vmax values as arguments.

``` python
import matplotlib.pyplot as plt
import numpy as np

data = np.random.rand(5,5) * 10

im = plt.imshow(data, cmap='viridis')
plt.colorbar()

im.set_clim(2,8)

plt.show()
```

In this example, we first create the plot as before, and then use the `set_clim()` method to limit the range of values in the colorbar to the interval [2,8].

## Method 3: Using norm parameter
Another method to set the colorbar range is by using a `Normalize` instance to map the data values to the colorbar values. We can pass in the `vmin` and `vmax` values to the `Normalize` instance.

``` python
import matplotlib.pyplot as plt
import numpy as np
from matplotlib.colors import Normalize

data = np.random.rand(5,5) * 10

norm = Normalize(vmin=2, vmax=8)
im = plt.imshow(data, cmap='viridis', norm=norm)
plt.colorbar()

plt.show()
```

In this example, we create a `Normalize` instance with the same `vmin` and `vmax` values as before. We then pass this `Normalize` instance to the `imshow()` method using the `norm` parameter.

## Conclusion
These are three different methods to set the colorbar range in Matplotlib in Python. By explicitly setting the range of values, we can have greater control over the visualization of our data.
