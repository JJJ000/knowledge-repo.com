---
title: Could you explain the meaning of %timeit in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: %timeit is a magic command in Jupyter notebooks that measures the time taken to execute a single line of code and provides the average time taken over multiple runs.
---

**Contents**

[TOC]

# Introduction

In Python, %timeit is a magic command that is used to measure the execution time of a code snippet. It is a powerful tool that helps optimize code by identifying bottlenecks and highlighting areas that need improvement.

# How to use %timeit

To use %timeit, simply write the code you want to measure performance for, followed by the %timeit command. For example:

```python
%timeit x = 10 + 20
```

This will return the average execution time of the code snippet over multiple runs.

# Parameters of %timeit

There are several parameters that can be passed to the %timeit command to customize its behavior, such as:

- `-n`: Number of loops to run. Default is 7.
- `-r`: Number of times to repeat the loop. Default is 3.
- `-t`: Number of seconds to run the loop. Default is 0.
- `-q`: Quiet mode. Suppresses output.
- `-o`: Returns the execution time as an object. 

For example, to run the loop 10 times and repeat it 5 times, you would use the following code:

```python
%timeit -n 10 -r 5 x = 10 + 20
```

# Conclusion

In conclusion, %timeit is a simple yet powerful tool for measuring the execution time of code in Python. It can be used to optimize code by identifying bottlenecks and highlighting areas that need improvement. With its customizable parameters, %timeit is a versatile tool that can be tailored to meet the specific needs of any project.
