---
title: Forming functions (or lambdas) iteratively (or through comprehension)
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: It is possible to create functions (or lambdas) in a loop (or comprehension) in Python using the `def` or `lambda` keyword and then call the function or lambda.
---

**Contents**

[TOC]

Section 1: Introduction

Python is a versatile programming language that allows developers to create and manipulate functions (or lambdas) in many ways. One common scenario is when there is a need to create a set of functions (or lambdas) in a loop (or comprehension). This could arise in situations where a set of similar tasks needs to be performed multiple times, with slightly different input parameters. In this article, we will explore different ways of creating functions (or lambdas) in a loop (or comprehension).

Section 2: Using lambda functions in a loop (or comprehension)

One of the easiest ways to create lambda functions in a loop (or comprehension) is by using the lambda keyword. For example, suppose we want to create a set of lambda functions that take two input arguments and return the sum of these arguments. We can achieve this using the following code:

```
funcs = [lambda a,b: a + b for i in range(5)]
```

In this code, we are creating a list of lambda functions called funcs. The range(5) part of the code specifies that we want to create 5 lambda functions. Inside the list comprehension, we use the lambda keyword to create the lambda functions. Each lambda function takes two input arguments a and b, and returns their sum.

Section 3: Using the functools.partial method

Another way to create functions in a loop (or comprehension) is by using the functools.partial method. This method allows us to create a new function from a pre-existing function by fixing some of its arguments. For example, suppose we have a function that returns the sum of three input arguments:

```
def sum_three(a, b, c):
    return a + b + c
```

Now suppose we want to create a list of functions that always sum two input numbers, but we want to use the previous function as a building block. We can achieve this using the functools.partial method:

```
from functools import partial

funcs = [partial(sum_three, c=0) for i in range(5)]
```

In this code, we are creating a list of functions called funcs. The range(5) part of the code specifies that we want to create 5 functions. Inside the list comprehension, we use the partial method to create the new functions. We pass the pre-existing function sum_three as the first argument, and we fix one of its input parameters (c) to 0.

Section 4: Using exec to create functions dynamically

A more advanced way of creating functions (or lambdas) in a loop (or comprehension) is by using the built-in exec function. This function allows us to execute a string of Python code dynamically. For example, suppose we want to create a set of lambda functions that take a single input argument n, and return the value of n^2. We can achieve this using the following code:

```
funcs = []

for i in range(5):
    code = 'lambda n: {}'.format(i**2)
    func = exec(code)
    funcs.append(func)
```

In this code, we are creating an empty list called funcs to store the lambda functions. We then use a for loop to iterate over a range of 5 numbers. Inside the loop, we create a string of Python code that defines a lambda function. The code variable is a string that contains the string 'lambda n: ' followed by the square of i. We then use the exec function to execute the code string and create a lambda function. Finally, we append the newly created lambda function to the funcs list. Note that the exec function returns None, so we cannot directly append its output to funcs. Instead, we must first create the lambda function and assign it to a variable called func.
