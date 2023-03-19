---
title: Could you tell me the counterpart of matlab's tic and toc functions in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: The Python equivalent of Matlab`s tic and toc functions is the time module`s time() function.
---

**Contents**

[TOC]

## Introduction
Matlab's tic and toc functions are used for measuring the execution time of a block of code in Matlab. The tic function starts the timer, and the toc function stops the timer and returns the elapsed time. Similarly, in Python, there are several ways to measure the execution time of a block of code. This article discusses some of the commonly used techniques to achieve this.

## Time Module
Python's time module provides a set of functions to work with the system time. The time.time() function returns the current time in seconds since the Epoch. Using this function, we can measure the elapsed time of a block of code. Here's an example:

```
import time

# Start the timer
start_time = time.time()

# Do some task
for i in range(10000):
    pass

# Stop the timer and print the elapsed time
elapsed_time = time.time() - start_time
print("Elapsed time: ", elapsed_time)
```

## Timeit Module
The timeit module provides a simple way to time small bits of Python code. It runs the code several times to get more accurate results and automatically disables the garbage collector during the timing. Here's an example:

```
import timeit

# Define the code to be timed
code = """
for i in range(10000):
    pass
"""

# Time the code and print the elapsed time
elapsed_time = timeit.timeit(code, number=1000)
print("Elapsed time: ", elapsed_time)
```

## datetime Module
Python's datetime module provides classes to work with dates and times. Using this module, we can measure the elapsed time of a block of code with high precision. Here's an example:

```
import datetime

# Get the current time
start_time = datetime.datetime.now()

# Do some task
for i in range(10000):
    pass

# Get the current time again and calculate the elapsed time
elapsed_time = datetime.datetime.now() - start_time
print("Elapsed time: ", elapsed_time.total_seconds())
```

## Conclusion
Python provides several ways to measure the execution time of a block of code, and the choice of technique depends on the specific requirements of the application. The time module provides a simple and lightweight way to measure the execution time, while the timeit module is well-suited for testing small code snippets. The datetime module provides high precision but is relatively more complex to use.
