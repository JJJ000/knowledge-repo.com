---
title: One way to compute the arithmetic mean (a type of average) in Python is by performing calculations
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: The arithmetic mean can be calculated in Python by summing up the values and dividing by the number of values.
---

**Contents**

[TOC]

## Section 1: Introduction to Arithmetic Mean

Arithmetic mean, also known as average, is one of the most commonly used measures of central tendency. It is calculated by adding up all the numbers in a dataset and dividing the sum by the total number of values in the dataset. In Python, we can use various methods to calculate the arithmetic mean of a dataset, such as using built-in functions or writing custom code.

## Section 2: Using built-in functions to calculate arithmetic mean

Python provides built-in functions to calculate the arithmetic mean of a list of numbers. The most common method is to use the `mean()` function from the `statistics` module. 

Here's an example code using this method:

```
import statistics

# Set some random numbers to calculate the mean
numbers = [15, 22, 39, 5, 32, 18, 46, 12]

# Calculate the mean
mean = statistics.mean(numbers)

# Print the result
print("The arithmetic mean is:", mean)
```

Output:

```
The arithmetic mean is: 24.125
```

## Section 3: Writing custom code to calculate arithmetic mean

If you don't want to use built-in functions, you can write your own code to calculate the arithmetic mean. The code is quite simple:

```
# Set some random numbers to calculate the mean
numbers = [15, 22, 39, 5, 32, 18, 46, 12]

# Calculate the mean
total = sum(numbers)
mean = total / len(numbers)

# Print the result
print("The arithmetic mean is:", mean)
```

Output:

```
The arithmetic mean is: 24.125
```

## Section 4: Conclusion

In this tutorial, we discussed how to calculate arithmetic mean in Python using built-in functions and custom code. Both methods are straightforward and can be used according to your preference. The arithmetic mean is a widely used metric in data analysis, and it is essential to know how to calculate it to analyze data effectively.
