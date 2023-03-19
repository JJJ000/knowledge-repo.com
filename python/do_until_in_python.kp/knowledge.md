---
title: Does Python have a "do ... until" construct?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: No, Python does not have a `do ... until` loop, but it has a similar function using the `while` loop with a true condition that is later broken by a conditional statement.
---

**Contents**

[TOC]

Introduction
------------

Python provides a number of control constructs to be used in loops, such as the traditional `while` and `for` loops. However, there is no built-in construct specifically designated as `do-until` loop in Python. In this article, we'll explore some ways to achieve similar functionality to a `do-until` loop in Python.

Using while loop
-----------------

One straightforward way to create a `do-until` loop in Python is to use a `while` loop where the condition is tested at the end, rather than at the beginning. Here is an example:

```python
condition = False

while True:
    # code to be executed in the loop
    # ...
    
    # check condition
    if condition:
        break
```

In this example, the loop will always execute at least once, because the condition is checked at the end. Once the condition is met, the loop is broken with the `break` statement.

Using a flag variable
---------------------

Another way to create a `do-until` loop in Python is to use a flag variable that is initialized as `True` and set to `False` once the loop has executed at least once. Here is an example:

```python
condition = False

while condition or first_loop:
    first_loop = False
    
    # code to be executed in the loop
    # ...
    
    # check condition
    if not condition:
        condition = True
```

In this example, the loop will execute at least once because the `condition` variable is initialized as `False`. After the first iteration, the `first_loop` variable is set to `False`, which causes the loop to continue executing as long as `condition` is `False`.

Using recursion
---------------

Another way to implement a `do-until` loop in Python is to use recursion. Here is an example:

```python
def my_loop():
    # code to be executed in the loop
    # ...
    
    # check condition
    if not condition:
        my_loop()

condition = False
my_loop()
```

In this example, the `my_loop()` function is called recursively as long as the `condition` variable is `False`. The loop will always execute at least once because the function is called the first time outside of the recursive function call. 

Conclusion
----------

Although there is no built-in syntax for a `do-until` loop in Python, we can use some techniques to achieve similar functionality. These include using a `while` loop with a condition checked at the end, using a flag variable, or using recursion.
