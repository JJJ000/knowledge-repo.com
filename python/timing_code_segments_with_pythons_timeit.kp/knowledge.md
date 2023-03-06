---
title: What is the process of using python's timeit to test the performance of a code segment?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the timeit function from the timeit module and pass in the code segment as a string argument.
---

**Contents**

[TOC]

## Introduction

`timeit` is a module in Python used for measuring the execution time of small code snippets. It provides a simple way of timing how long it takes for a piece of code to execute. In this tutorial, we will see how to time a code segment for testing performance using Python's `timeit` module.

## Importing the timeit module

Before we begin timing our code segment, we need to import the `timeit` module.

```python
import timeit
```

## Using the timeit function

The `timeit` module provides a function also called `timeit` that we can use to time a code segment. The function takes several arguments that we can use to customize how the timing is done. Here's an example:

```python
code = """
a = []
for i in range(100000):
    a.append(i)
"""

time = timeit.timeit(code, number=100)
print("Time taken: ", time)
```

In this example, we want to time how long it takes to create a list of 100,000 numbers. We first define the code segment as a string and store it in the `code` variable. We then call the `timeit` function and pass in the `code` variable as the first argument. The `number` argument specifies the number of times to execute the code segment. In this case, we want to execute it 100 times. Finally, we print out the result of the timing.

## Using setup code

Sometimes, the code we want to time might depend on other code that needs to be executed first. We can provide this setup code to the `timeit` function using the `setup` argument. Here's an example:

```python
setup = """
import random
a = [random.randint(1, 1000) for _ in range(100000)]
"""

code = """
a.sort()
"""

time = timeit.timeit(code, setup=setup, number=100)
print("Time taken: ", time)
```

In this example, we want to time how long it takes to sort a list of 100,000 random numbers. We first define the setup code as a string and store it in the `setup` variable. This sets up a list `a` containing 100,000 random numbers between 1 and 1000. We then define the code we want to time, which is to sort the list `a`. We then call the `timeit` function, passing in the `code`, `setup`, and `number` arguments. Finally, we print out the result of the timing.

## Conclusion

In this tutorial, we've seen how to time a code segment for testing performance using Python's `timeit` module. We can use the `timeit` function to time a code segment and customize the timing by specifying the number of times to execute the code and providing setup code if necessary. By timing our code, we can identify which parts are taking the most time and optimize them for better performance.
