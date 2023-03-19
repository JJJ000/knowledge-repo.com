---
title: To test the except block, one can use a function mock to raise an exception
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Use the `mock` library to replace the function with a mock that raises the desired exception, then call the function in a `try` block with the expected `except` block.
---

**Contents**

[TOC]

## Introduction
In this tutorial, we will discuss how to mock a function to raise an exception to test an except block in Python. This is an important testing technique that helps us ensure the robustness of our code and identify any potential errors or bugs.

## Creating a Simple Function

First, let's create a simple function that we can use to demonstrate how to mock it to raise an exception. Here's the code for our function:

```python
def divide(x,y):
    try:
        result = x/y
    except ZeroDivisionError:
        print("Error: Cannot divide by zero!")
    else:
        return result
```

This function takes two arguments, `x` and `y`, and attempts to divide `x` by `y`. If `y` is zero, it raises a `ZeroDivisionError` exception and prints an error message. Otherwise, it returns the result of the division.

## Mocking the Function to Raise an Exception

Now, let's say we want to test the `except` block of our `divide` function. To do this, we need to mock the function so that it raises a `ZeroDivisionError` exception. Here's how we can do that:

```python
import unittest.mock as mock

def test_divide_exception():
    with mock.patch('__main__.divide') as mock_divide:
        mock_divide.side_effect = ZeroDivisionError()
        divide(4,0)
        mock_divide.assert_called_once_with(4,0)
```
In this code, we first import the `unittest.mock` module, which provides us with tools for mocking functions.

We then use the `mock.patch` function to patch our `divide` function with a mock object. This creates a new version of the `divide` function that we can use in our test.

We set the `side_effect` attribute of the mock object to a `ZeroDivisionError` instance. This causes the mock function to raise a `ZeroDivisionError` exception whenever it is called.

Finally, we call our `divide` function with the arguments `4` and `0`. This should cause the `except` block of our `divide` function to be executed, since we are now mocking the function to raise a `ZeroDivisionError` exception.

We then use the `mock_divide.assert_called_once_with(4,0)`  function to verify that our mock function was called once with the correct arguments.

## Conclusion

In this tutorial, we discussed how to mock a function to raise an exception to test an `except` block in Python. We also provided an example of how to use this technique to test the `divide` function, which demonstrates the power and flexibility of the Python `unittest.mock` module.
