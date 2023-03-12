---
title: Determine the amount of time the Python script took to finish executing
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the time module to record the start and end time of the script, then take their difference to find the total execution time.
---

**Contents**

[TOC]

# Method 1: Using time module

The easiest way to determine the time taken for a Python script to execute is to use the `time` module. Here is the sample code:

```python
import time

start = time.time()

# your code here

end = time.time()
print('Time taken:', end - start)
```

You can replace `# your code here` with your actual code. The `time.time()` function returns the current timestamp in seconds since the epoch. Subtracting the start timestamp from the end timestamp will give you the time taken in seconds. 

# Method 2: Using datetime module

Another way to measure the execution time of a Python script is to use the `datetime` module. Here is the sample code:

```python
import datetime

start = datetime.datetime.now()

# your code here

end = datetime.datetime.now()
print('Time taken:', end - start)
```

This method uses the `datetime.datetime.now()` function to get the current timestamp. The difference between the start and end timestamps will give you the time taken in seconds.

# Method 3: Using timeit module

The `timeit` module provides a more accurate way to measure the execution time of small code snippets. Here is the sample code:

```python
import timeit

code_to_measure = '''
# your code here
'''

time_taken = timeit.timeit(stmt=code_to_measure, number=1000)
print('Time taken:', time_taken)
```

Replace `# your code here` with the code you want to measure. The `stmt` argument specifies the code to measure, and the `number` argument specifies the number of times to run the code. The `timeit.timeit()` function returns the time taken in seconds.

# Method 4: Using profiling tools

Profiling tools such as cProfile and PyCharm's built-in profiler can be used to measure the execution time of your Python code. These tools provide detailed information about the time taken by each function and line of code. However, they require some setup and configuration, and may not be suitable for quick measurements.
