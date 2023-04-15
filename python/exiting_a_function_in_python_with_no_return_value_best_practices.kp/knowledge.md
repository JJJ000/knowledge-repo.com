---
title: What approach can one take in Python to exit a function that lacks a return value before it completes (such as when a condition is not met)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `return` keyword with no return value to exit the function.
---

**Contents**

[TOC]

There are a few ways to exit a Python function before it finishes execution, depending on the situation. Here are three possible solutions:

## Using a Simple 'if' Statement

One way to exit a function prematurely is to use an 'if' statement and the 'return' statement inside a code block. The 'if' statement checks for some condition that, if true, triggers the 'return' statement, which will immediately exit the function.

```python
def some_function(some_argument):
    if some_condition:
        return
    # rest of the function here
```

## Raising an Exception

Another option is to raise an exception when some condition is met. This will also cause the function to exit immediately.

```python
def some_function(some_argument):
    if some_condition:
        raise ValueError('Some error message.')
    # rest of the function here
```

This will raise a ValueError exception with the specified message, which can be caught and handled by the calling code if necessary.

## Using 'assert'

The 'assert' statement is another option for exiting a function early. This statement checks for a certain condition and raises an AssertionError if it evaluates to false. 

```python
def some_function(some_argument):
    assert some_condition, 'Some error message.'
    # rest of the function here
```

If the assertion fails, the assertion message will be printed and the function will exit immediately. This can be useful for debugging and enforcing assumptions in code, but may not be appropriate for every situation.

## Conclusion

These are three ways to exit a Python function before it completes execution, depending on the desired behavior and reason for exiting. Using a simple 'if' statement, raising an exception, and using 'assert' can all be effective tools for handling unexpected situations in code.
