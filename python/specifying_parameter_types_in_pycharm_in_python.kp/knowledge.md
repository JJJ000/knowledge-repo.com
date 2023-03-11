---
title: What is the method for informing pycharm about the expected type of a parameter?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Use type annotations to tell PyCharm what type a parameter is expected to be in Python.
---

**Contents**

[TOC]

# Use Type Hints
One way to tell PyCharm what type a parameter is expected to be in Python is to use type hints. 

Type hints are annotations that can be added to function parameters, indicating the expected data type for that parameter. PyCharm can then use these type hints to provide more accurate code completion suggestions and catch type-related errors during code analysis. 

Here's an example of a function with a type hint: 

```
def calculate_total(num_items: int, price: float) -> float:
    return num_items * price
```

In this example, the `num_items` parameter is annotated with the `int` type hint, indicating that it should be an integer. The `price` parameter is annotated with the `float` type hint, indicating that it should be a floating-point number. 

The function also has a return type hint of `float`, indicating that the function will return a floating-point number. 

# Use Docstrings
Another way to indicate the expected type of a parameter in PyCharm is to use a docstring. 

Docstrings are multi-line comments that appear at the beginning of a function, module, or class definition. They provide a description of the code and can include information about the expected data types of function parameters. 

Here's an example:

```
def calculate_total(num_items, price):
    """
    Calculates the total cost of a given number of items at a given price.

    Parameters:
    num_items (int): The number of items to calculate the cost for.
    price (float): The price per item.

    Returns:
    float: The total cost of the items.
    """
    return num_items * price
```

In this example, the docstring provides a description of what the function does, as well as information about the expected data types of the `num_items` and `price` parameters. 

# Use Type Checking Libraries
Finally, PyCharm can also support type checking libraries, such as `mypy`. 

`mypy` is a type checker for Python that can be used to statically analyze code and catch type-related errors. PyCharm can be configured to use `mypy` to check for type errors in your code. 

Here's an example:

```
# mypy_example.py
def greet(name: str) -> str:
    return 'Hello, ' + name
```

In this example, the `greet` function takes a parameter named `name`, which is annotated with the `str` type hint. The function also has a return type hint of `str`. 

When this code is run through `mypy`, any type errors (e.g. passing an integer instead of a string) will be caught and reported. PyCharm can also use `mypy` and show type errors in real time.
