---
title: Testing the speed of Python by calculating the difference in time, measuring it in milliseconds
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Python`s time module provides a way to calculate the time difference in milliseconds between two events.
---

**Contents**

[TOC]

## Introduction
Speed testing code in Python is an essential step towards optimizing the code for better performance. Python provides various functions and modules to perform such speed testing, including the time module and the timeit module. These modules provide different techniques to measure the time difference between two events or chunks of code. 

This article discusses how to measure time differences in milliseconds using Python.

## Using the time module
The simplest way to measure the time difference in milliseconds is by using the `time` module. Here's an example:

```python
import time

start_time = time.time()

# code to be tested

end_time = time.time()

time_diff_ms = (end_time - start_time) * 1000
print(f"Time difference: {time_diff_ms} ms")
```

The `time()` function returns the current time in seconds since the epoch, which is a float value. We can capture the start and end times of the code that needs to be tested in `start_time` and `end_time` variables, respectively. Then, we can subtract the start time from the end time to get the time difference in seconds. Finally, we multiply the result with 1000 to convert it to milliseconds.

## Using the timeit module
The `timeit` module provides a more robust way of measuring the execution time of a piece of code. It offers two methods to measure the time difference: `timeit()` and `repeat()`. Here's an example using `timeit()`:

```python
import timeit

stmt = """
# code to be tested
"""

time_diff_ms = timeit.timeit(stmt=stmt, number=100) * 10
print(f"Time difference: {time_diff_ms} ms")
```

Here, we define a string `stmt` that contains the code to be tested. We can pass this string to the `timeit()` function, along with the `number` parameter, which specifies the number of times the code should be executed. The `timeit()` function returns the total time taken for all executions. We can multiply this result with 10 to get the time difference in milliseconds.

## Using a performance profiling tool
Another way to measure the time difference in milliseconds is by using a performance profiling tool. Python provides multiple profiling tools, including `cProfile`, `line_profiler`, and `py-spy`. These tools let you measure the time taken by individual functions or lines of code. Here's an example using `cProfile`:

```python
import cProfile

def function_to_test():
    # code to be tested

pr = cProfile.Profile()
pr.enable()

function_to_test()

pr.disable()

pr.print_stats(sort="time")
```

Here, we define a function `function_to_test` that contains the code to be tested. We can use the `cProfile` module to measure the time taken by this function. The `pr.enable()` and `pr.disable()` functions start and stop the profiler. Finally, we use the `pr.print_stats()` function to print the profiling results, sorted by the time taken.

## Conclusion
In this article, we discussed three ways to measure the time difference in milliseconds in Python. We learned that the `time` module provides a simple way to measure time differences, whereas the `timeit` module offers more robust options. We also explored using a performance profiling tool like `cProfile` to measure the time taken by individual functions or lines of code. Depending on your use case, you can choose the method that suits you the best.
