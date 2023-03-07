---
title: Create a set of numbers with a specified numerical distribution using randomization
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the random module in Python and specify the desired distribution with functions such as random.gauss() for a Gaussian distribution or random.expovariate() for an exponential distribution.
---

**Contents**

[TOC]

## Section 1: Introduction
Generating random numbers with a given distribution is a common task in data analysis and simulation. In Python, the `numpy.random` module provides a variety of functions for generating random numbers that follow different distributions. In this tutorial, we will demonstrate how to generate random numbers with a given numerical distribution in Python.

## Section 2: Generating random numbers with a uniform distribution
The simplest type of random distribution is the uniform distribution, where each value has an equal probability of being selected. In Python, we can use the `numpy.random.uniform()` function to generate random numbers with a uniform distribution. The function takes two arguments, the minimum and maximum values of the distribution, and returns an array of random numbers.

```python
import numpy as np

# Generate 10 random numbers between 0 and 1
uniform_numbers = np.random.uniform(0, 1, 10)
print(uniform_numbers)
```

Output:
```
[0.53570971 0.51775379 0.63802426 0.7230975  0.91473632 0.66206828
 0.35990728 0.42982704 0.25454314 0.85486793]
```

## Section 3: Generating random numbers with other distributions
In addition to the uniform distribution, there are many other types of distributions that can be used to generate random numbers with specific properties. For example, the normal distribution is a common distribution where values cluster around a mean and have a certain standard deviation.

To generate random numbers with a normal distribution, we can use the `numpy.random.normal()` function. This function takes three arguments: the mean value of the distribution, the standard deviation, and the number of random numbers to generate.

```python
# Generate 10 random numbers with a normal distribution
normal_numbers = np.random.normal(0, 1, 10)
print(normal_numbers)
```

Output:
```
[ 1.84575737 -1.6212477  -0.97647307  0.10208351  0.72322815  1.51054106
 -1.47853986 -0.34347043 -0.77054631  1.27537192]
```

## Section 4: Generating random numbers with discrete distributions
Sometimes we want to generate random numbers with a discrete distribution, where the values can only take on specific, discrete values. For example, if we are simulating a roll of a six-sided die, we want to generate random numbers that can only take on the values 1 through 6.

To generate random numbers with a discrete distribution, we can use the `numpy.random.choice()` function. This function takes two arguments: an array of possible values, and the number of random numbers to generate. The function returns an array of random values chosen from the input array.

```python
# Generate 10 random numbers with a discrete distribution
dice_numbers = np.random.choice([1, 2, 3, 4, 5, 6], 10)
print(dice_numbers)
```

Output:
```
[2 2 1 1 5 5 3 3 1 3]
```

## Section 5: Conclusion
In this tutorial, we have demonstrated how to generate random numbers with various numerical distributions in Python using the `numpy.random` module. We covered generating random numbers with a uniform distribution, a normal distribution, and a discrete distribution. These functions are powerful tools for generating random data for analysis and simulation.
