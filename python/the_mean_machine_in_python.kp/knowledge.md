---
title: Averages that move or means that run
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: A moving average, also called a running mean, can be implemented in Python using the pandas library with the rolling() method.
---

**Contents**

[TOC]

Introduction to Moving Average/Running Mean

Moving Average or Running Mean is a widely used statistical method to analyze time series data. It helps us to identify patterns in data and is used in various fields such as finance, economics, and meteorology. The moving average is calculated by taking the average of a fixed number of data points at a time.

In Python, we can easily calculate the moving average using different libraries like NumPy, Pandas, or even plain Python code.

Calculating Moving Average in NumPy

NumPy is a popular library in the Python ecosystem used for scientific computing. NumPy provides a built-in method for calculating the moving average of an array or a list.

```
import numpy as np

data = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
window_size = 3

def moving_average(data, window_size):
    weights = np.repeat(1.0, window_size)/window_size
    smas = np.convolve(data, weights, 'valid')
    return smas

MA = moving_average(data, window_size)
print(MA)
```

Output:

```
[ 2.  3.  4.  5.  6.  7.  8.]
```

Here, we first define our data as a list. We then define the window size, which is how many data points we want to consider at once for calculating the moving average. We then define a function “moving_average” that takes in data and window size as parameters. Inside this function, we first create a “weights” array, which is simply an array of 1s of length “window_size” divided by “window_size”. We then use the convolve() method to calculate the moving average using the data and weights. Finally, we return this calculated moving average.

Calculating Moving Average in Pandas

Pandas is a popular data manipulation library that provides various functions for data analysis. We can also use the rolling() function in Pandas to calculate the moving average.

```
import pandas as pd

data = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
window_size = 3

df = pd.DataFrame(data)
MA = df.rolling(window=window_size).mean()
print(MA)
```

Output:

```
     0
0  NaN
1  NaN
2  2.0
3  3.0
4  4.0
5  5.0
6  6.0
7  7.0
8  8.0
9  9.0
```

Here, we first define our data as a list. We then define the window size, which is how many data points we want to consider at once for calculating the moving average. We then convert the data to a Pandas dataframe and use the rolling() function to calculate the moving average. Finally, we print the calculated moving average.

Conclusion

In this article, we learned how to calculate the moving average using different libraries in Python. We used NumPy and Pandas to calculate the moving average, which are popular libraries in the Python ecosystem. We also saw that calculating the moving average is a simple task in Python that can be done in just a few lines of code.
