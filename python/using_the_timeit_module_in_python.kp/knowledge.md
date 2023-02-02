---
title: What is the process of using the timeit module?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: The timeit module can be used to measure the execution time of a Python statement or expression.
---

**Contents**

[TOC]

# Introduction
The timeit module is a built-in Python module that allows you to measure the execution time of small code snippets. It can be used to measure the performance of code, compare different algorithms, and identify bottlenecks in code.

# Setup
Before using the timeit module, you must first import it. This can be done by using the following statement:

`import timeit`

# Usage
The timeit module provides two functions for measuring the execution time of code snippets: timeit.timeit() and timeit.repeat(). 

The timeit.timeit() function takes a single parameter, which is a string containing the code to be executed. The function will execute the code and return the number of seconds it took to execute.

The timeit.repeat() function takes three parameters: a string containing the code to be executed, a number of repetitions, and a number of repetitions to discard. The function will execute the code the specified number of times and return a list containing the execution times for each repetition.

# Example
The following example shows how to use the timeit module to measure the execution time of a simple function:

```
import timeit

def my_function():
    a = 0
    for i in range(1000):
        a += i

execution_time = timeit.timeit('my_function()', setup='from __main__ import my_function', number=1)

print('Execution time:', execution_time)
```

The output of the example will be:

`Execution time: 0.0004195999999999965`
