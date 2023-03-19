---
title: Can you provide a guide on computing the rolling/moving average utilizing Python and numpy/scipy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the rolling() method from pandas library, along with the mean() method to calculate the rolling / moving average in Python.
---

**Contents**

[TOC]

Section 1: Introduction
Calculating rolling / moving averages is a common operation in time series analysis. Moving averages are useful for smoothing out noise in the data and identifying trends. In this tutorial, we will learn how to calculate rolling / moving averages using Python with the NumPy and SciPy libraries.

Section 2: Creating sample data
To demonstrate the calculation of rolling / moving averages, we will first create some sample data. We will generate 1000 random numbers between 0 and 1 using NumPy's random module:

```python
import numpy as np

# generate a random dataset of 1000 values between 0 and 1
np.random.seed(42)
data = np.random.rand(1000)
```

Section 3: Calculating rolling / moving averages
We can calculate rolling / moving averages using the `rolling` function from pandas or the `convolve` function from numpy. In this tutorial, we will use the `convolve` function from numpy to calculate the moving averages.

```python
import numpy as np
from numpy.convolution import convolve

# define the window size
window_size = 10

# calculate the moving average using the convolve function
moving_average = np.convolve(data, np.ones(window_size)/window_size, mode='valid')
```

In the above code, we first define the window size as `10`. This means that we will calculate the moving average of 10 consecutive points in the dataset. We then use the `convolve` function from numpy to calculate the moving average. The `mode` argument is set to `'valid'` to ensure that the output only contains valid values.

Section 4: Plotting the results
To visualize the results, we can plot the original dataset and the moving average using the matplotlib library:

```python
import matplotlib.pyplot as plt

# plot the original dataset and the moving average
plt.plot(data, label='Original Data')
plt.plot(moving_average, label=f'Moving Average (window size={window_size})')
plt.legend()
plt.show()
```

In the above code, we first import the `pyplot` module from matplotlib. We then plot the original dataset and the moving average using the `plot` function from `pyplot`. We also add a label for the moving average that shows the window size used for the calculation. Finally, we call the `legend` function to show the legend and the `show` function to display the plot.

Conclusion:
In this tutorial, we learned how to calculate rolling / moving averages in Python using the NumPy and SciPy libraries. We generated some sample data, calculated the moving average using the `convolve` function from numpy, and plotted the results using the matplotlib library. Moving averages are useful for smoothing out noise in the data and identifying trends, and they are commonly used in time series analysis.
