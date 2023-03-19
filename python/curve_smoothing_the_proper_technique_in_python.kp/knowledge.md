---
title: What is the proper way to make a curve smoother?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use a curve fitting function such as scipy`s `scipy.optimize.curve\_fit` to find the best-fitting function to approximate the curve and plot the smoothed curve using this function.
---

**Contents**

[TOC]

## Overview
One way to smooth a curve in Python is by using a function from the scipy library called `savgol_filter()`. However, it is important to understand the parameters and their significance in order to achieve the desired smoothing effect.

### 1. Understanding the `savgol_filter()` function
The `savgol_filter()` function is used for signal processing and smoothing noisy data. It applies a smoothing filter to a one-dimensional array of data. The function uses a least-squares polynomial fit to smooth out the curve, which helps to reduce the effect of noise while preserving the shape of the curve.

In order to use `savgol_filter()`, we need to understand its parameters. The main parameters are:
- `window_length`: The length of the window over which the polynomial function is fitted. The window size should be odd and greater than 2, e.g., 3, 5, 7, etc.
- `polyorder`: The order of the polynomial function used to fit the data. A value of 0 corresponds to a moving average filter, while a value of 1 corresponds to a linear filter. A higher order value will fit a more complex function to the data. 

### 2. Choosing the appropriate `window_length` and `polyorder`
Choosing the appropriate `window_length` and `polyorder` values can have a significant impact on the smoothing effect. 

In general, a larger `window_length` will result in a smoother curve, but with more distortion in the shape of the curve. Too large a `window_length` can result in over-smoothing or even loss of important features of the curve. A smaller window length will preserve the shape better, but may not smooth out the noise sufficiently. It is important to choose the `window_length` depending on the noise level in the data and the desired level of smoothing.

Similarly, a higher `polyorder` will result in a more complex fit and can better preserve the shape of the curve. However, it can also result in overfitting, and may not always be necessary. For most cases, a `polyorder` of 1 or 2 is sufficient.

### 3. Applying the `savgol_filter()` function
To apply the `savgol_filter()` function, we first import it from the `scipy.signal` module. We can then simply call the function and pass in the data that needs to be smoothed along with the window length and polyorder parameters.

For example:
```python
from scipy.signal import savgol_filter
y_smooth = savgol_filter(y, window_length=5, polyorder=1)
```
Here, a `window_length` of 5 and a `polyorder` of 1 is used to smooth out the curve represented by the `y` data array. The smoothed curve is stored in the `y_smooth` array.

### 4. Visualizing the smoothed curve
Finally, we can visualize the smoothed curve using a plotting library such as `matplotlib`. Here's an example:
```python
import matplotlib.pyplot as plt
plt.plot(x, y, label='Original')
plt.plot(x, y_smooth, label='Smoothed')
plt.legend()
plt.show()
```
This code will plot the original curve (`x` vs `y`) as well as the smoothed curve (`x` vs `y_smooth`) on the same figure with a legend. 

## Conclusion
Smoothing a curve in Python can be achieved using the `savgol_filter()` function from the `scipy` library. It is important to choose the appropriate `window_length` and `polyorder` parameters depending on the level of noise in the data and the desired level of smoothing. Finally, the smoothed curve can be visualized using a plotting library such as `matplotlib`.
