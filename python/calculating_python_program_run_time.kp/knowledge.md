---
title: What is the method to compute the running time of a program in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the time module`s `time` function to calculate the difference between the start and end times of the program.
---

**Contents**

[TOC]

## Using time library

One of the easiest ways to calculate the run time of a Python program is by using the time library. You can start a timer before the code you want to measure, and stop it immediately after. The difference between the two times will give you the program's run time.

```python
import time

start_time = time.time()

# your code here

print("--- %s seconds ---" % (time.time() - start_time))
```

The output will be something like: `--- 0.0021657943725585938 seconds ---`


## Using datetime library

Another way to calculate program run time is using the datetime library. You can create two datetime objects before and after running the code, and subtract one from the other to get the elapsed time.

```python
import datetime

start_time = datetime.datetime.now()

# your code here

end_time = datetime.datetime.now()
elapsed_time = end_time - start_time

print(f"Elapsed time: {elapsed_time}")
```

The output will be something like: `Elapsed time: 0:00:00.001478`


## Using timeit library

The timeit library provides a way to run a function or piece of code multiple times and calculate the average run time. This is useful when you want to test the performance of your code under different conditions.

```python
import timeit

def my_function():
    # your code here

print(timeit.timeit(my_function, number=100))
```

The `number` argument specifies how many times to run the function. The output will be the average run time of each function call.


## Using profile/cProfile modules

The profile/cProfile modules allow you to analyze the performance of your Python code in much more detail, by producing a detailed report of the function calls and the time spent in each of them.

```python
import cProfile

def my_function():
    # your code here

cProfile.run('my_function()')
```

This will output a detailed report of the function calls and the time spent in each of them. This is useful for identifying bottlenecks in your code and optimizing it for better performance.
