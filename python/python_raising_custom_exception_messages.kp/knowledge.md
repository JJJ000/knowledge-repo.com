---
title: In python, what is the method to generate an exception along with a personalized message that is the same as the original exception?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can raise the same exception with a custom message using the raise statement and passing in the exception class and the custom message as arguments.
---

**Contents**

[TOC]

## Use Case

Python has various built-in exceptions that are raised when an error occurs. Sometimes we may need to raise the same exception, but with a custom message. There are various reasons we might want to do that, such as adding more context or information about the error or creating our custom error handling logic.

In this guide, we will discuss how to raise the same exception with a custom message in Python.


## Using the `raise` Keyword

The `raise` keyword in Python is used to raise an exception manually. We use it in combination with exception classes, such as `ValueError`, `TypeError`, or `Exception`. We can raise an exception with a custom message by passing a string message to the constructor of an exception class.


Consider the following example:

```python
def divide_numbers(num1, num2):
    if num2 == 0:
        raise ValueError("Cannot divide by zero.")
    return num1 / num2
```

In this example, we are raising a `ValueError` exception whenever a zero value is passed as the second argument to the `divide_numbers` function. We are passing a custom message "Cannot divide by zero" to the constructor of the `ValueError` exception class. Now, whenever this exception is raised, the message "Cannot divide by zero" will be displayed.


## Creating a Custom Exception Class

Sometimes, we might need more specific exceptions that are not pre-defined in Python. We can create a custom exception class that inherits from the `Exception` class or any of its subclasses. We can then raise this custom exception by using the `raise` keyword.


Consider the following example:

```python
class NegativeNumberError(Exception):
    pass

def cuberoot(number):
    if number < 0:
        raise NegativeNumberError("Cannot calculate the cube root of a negative number.")
    return number ** (1/3)
```

In this example, we are creating a custom exception class called `NegativeNumberError` that inherits from the `Exception` class. We also have a function called `cuberoot` that raises this exception whenever it receives a negative number as input. We are passing a custom message "Cannot calculate the cube root of a negative number" to the constructor of our custom exception class. Now, whenever we raise this exception, the message will be displayed, along with the appropriate traceback.


## Reraising an Exception with a Custom Message

Sometimes we might want to catch an exception, add some additional information or processing, and then raise the same exception with a custom message. We can do this by using the `raise` keyword within an exception handler block and passing the caught exception object.

Consider the following example:

```python
try:
    a = 10
    b = 0
    c = a / b
except ZeroDivisionError as e:
    raise ZeroDivisionError("Cannot divide by zero. Please provide a non-zero value.") from e
```

In this example, we are catching the `ZeroDivisionError` exception and adding a custom message "Cannot divide by zero. Please provide a non-zero value." to it. We are using the `from` keyword to link the caught exception with the new exception that we are raising. This is useful because it preserves the original error information, making it easier to debug. Now, whenever we raise this exception, the new message will be displayed, along with the original traceback.
