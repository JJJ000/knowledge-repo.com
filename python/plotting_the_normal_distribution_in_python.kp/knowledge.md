---
title: What is the process of graphing a normal distribution?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the pyplot module from the matplotlib library to plot a normal distribution by specifying the mean and standard deviation values and generating a set of random numbers using the numpy library.
---

**Contents**

[TOC]

Section 1: Introduction to Normal Distribution
---

Normal distribution, also known as Gaussian distribution, is a probability distribution that is widely used in various fields, such as statistics, physics, economics, and engineering. It is called normal distribution because it is the most common type of distribution encountered in nature. The normal distribution has a bell-shaped curve that follows a specific mathematical formula, which allows us to calculate the probability of getting a certain value within a given range.

Section 2: Creating a Normal Distribution in Python
---

To plot a normal distribution in Python, we will need to use the NumPy and Matplotlib libraries. We can use the NumPy random module to generate a set of random numbers that follow a normal distribution. Then, we can use Matplotlib to plot the distribution.

Here's an example code:

```python
import numpy as np
import matplotlib.pyplot as plt

# Generate random numbers from a normal distribution
mu, sigma = 0, 0.1 # mean and standard deviation
s = np.random.normal(mu, sigma, 1000)

# Plot histogram
count, bins, ignored = plt.hist(s, 30, density=True)

# Plot the distribution curve
plt.plot(bins, 1/(sigma * np.sqrt(2 * np.pi)) * np.exp(-(bins - mu)**2 / (2 * sigma**2)), linewidth=2, color='r')

# Show plot
plt.show()
```

This code will generate 1000 random numbers that follow a normal distribution with a mean of 0 and a standard deviation of 0.1. Then, it will plot a histogram of these numbers along with the probability distribution curve. The `density=True` argument in the `plt.hist()` function will normalize the histogram so that the area under the curve equals to 1.

Section 3: Interpretation of the Normal Distribution Plot
---

The resulting plot will have a bell-shaped curve that is centered around the mean value (in this case, 0). The curve will be symmetrical and the tails will extend infinitely in both directions.

The area under the curve represents the probability of getting a certain value within a given range. For example, the area under the curve between -1 and 1 represents the probability of getting a value between -1 and 1. The total area under the curve equals to 1, which means that the probability of getting any value within the distribution is 1.

Section 4: Conclusion
---

Plotting a normal distribution in Python is a useful way to visualize a probability distribution and calculate the probability of getting a certain value within a given range. It can be used in various fields, such as statistics, physics, economics, and engineering, to analyze data and make predictions.
