---
title: Algorithm to detect the highest point using python/scipy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: The `scipy.signal.find\_peaks` function is a peak-finding algorithm in Python/SciPy.
---

**Contents**

[TOC]

Section 1: Introduction to Peak-Finding Algorithm

A peak-finding algorithm is a method used to identify the highest points (peaks) in a data set. It is commonly used in signal processing, image analysis, and data mining. In Python, there are several libraries that can be used for this task, including NumPy, SciPy, and Pandas. In this article, we will focus on how to use SciPy library for peak detection.

Section 2: Using SciPy's find_peaks() function

SciPy's find_peaks() function is a powerful tool for identifying peaks in a signal. It uses a technique called "hill-climbing" to find local maxima in a signal. The function takes various parameters, such as the threshold value for peak detection, and the minimum and maximum distance between peaks.

Here's an example code snippet that demonstrates how to use find_peaks() to identify peaks in a data set:

```python
import numpy as np
from scipy.signal import find_peaks

# Generate some test data
t = np.linspace(0, 2 * np.pi, 1000)
x = np.sin(5 * t)

# Find peaks in the data
peaks, _ = find_peaks(x, height=0)

# Plot the data and markers at the peaks
import matplotlib.pyplot as plt
plt.plot(t, x)
plt.plot(t[peaks], x[peaks], "x")
plt.show()
```

This code generates a test dataset (a sine wave), and then identifies the peaks in the signal using find_peaks(). The resulting peaks are then plotted on the same graph.

Section 3: Using find_peaks_cwt() function

Another function from SciPy that can be used to detect peaks is find_peaks_cwt(). This function uses a technique called "continuous wavelet transform" to find peaks in the signal. The function takes a signal as input, as well as various parameters that control the size and shape of the wavelet used for peak detection.

Here's an example of how to use find_peaks_cwt() to detect peaks in a data set:

```python
import numpy as np
from scipy.signal import find_peaks_cwt

# Generate some test data
t = np.linspace(0, 2 * np.pi, 1000)
x = np.sin(5 * t)

# Find peaks in the data
peaks = find_peaks_cwt(x, np.arange(1, 10))

# Plot the data and markers at the peaks
import matplotlib.pyplot as plt
plt.plot(t, x)
plt.plot(t[peaks], x[peaks], "x")
plt.show()
```

This code generates a test dataset (a sine wave), and then identifies the peaks in the signal using find_peaks_cwt(). The resulting peaks are then plotted on the same graph.

Section 4: Conclusion

In this article, we looked at two different functions from SciPy that can be used to detect peaks in a signal. These functions can be used to identify important features in a data set, and can be useful in a variety of applications. By understanding how these functions work and how to use them, you can improve your data analysis and signal processing skills.
