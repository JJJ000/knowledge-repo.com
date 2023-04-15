---
title: What is the process to write documentation for a method that contains one or more parameter(s)?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use a docstring to describe the input(s) and output(s) of the method, including any expected data types or value ranges.
---

**Contents**

[TOC]

# Python Method Documentation with Parameters

When writing code in Python, it is essential to document classes and methods clearly. Documenting code helps in understanding the functionality of the code, making it easier for others to work with the codebase. One of the key components of documenting functions is specifying parameters. In this article, we will discuss how to document a method with parameters in Python. 

## 1. Naming Conventions
Before we begin, it is essential to follow good naming conventions while specifying parameters. It is recommended to use self-explanatory names for parameters. A parameter's name must start with a lowercase letter and use underscores to delimit words. 

```python
def calculate_discounted_price(original_price: float, discount_percentage: float) -> float:
    """
    Calculates the discounted price given the original price and discount percentage.

    :param original_price: The original price of the product.
    :param discount_percentage: The discount percentage to be applied to the original price.
    :return: The discounted price of the product.
    """
    discounted_price = original_price - ((discount_percentage / 100) * original_price)
    return discounted_price
```

## 2. Docstring Format
Python's built-in documentation tool, **Docstrings**, provides a simple and convenient way of documenting code. Docstrings are enclosed within triple quotes, and this format can be used to provide documentation for the function, class, module, or package. 

When documenting functions or methods, we need to include a docstring that is located immediately after the function definition. In the docstring, we specify the objective, the parameters, and the return value of the function. 
```python
def calculate_discounted_price(original_price: float, discount_percentage: float) -> float:
    """
    Calculates the discounted price given the original price and discount percentage.

    :param original_price: The original price of the product.
    :type original_price: float

    :param discount_percentage: The discount percentage to be applied to the original price.
    :type discount_percentage: float

    :return: The discounted price of the product.
    :rtype: float
    """
 
    discounted_price = original_price - ((discount_percentage / 100) * original_price)
    return discounted_price
```

## 3. Parameter Annotations
In Python, you can annotate the function's parameter's data types by adding them after the parameter name with a colon. It is the most effective way to specify the type of input the function expects. We can also specify the data type of the function's return value using the `->` notation before the function's final colon. 

```python
def calculate_discounted_price(original_price: float, discount_percentage: float) -> float
```

## 4. Auto-Documentation
Another way to generate documentation for your code is by using an automated documentation tool. These tools extract code documentation from your codebase and generate HTML, PDF, or Markdown documents. 

- **Sphinx:** A popular documentation tool for Python code that is used by many open-source projects. Sphinx uses reStructuredText (reST) format and supports autodoc, system messages, and doesn't require external dependencies.
- **Pycco:** Generatates documentation for Python, CoffeeScript, and JavaScript. Code comments are displayed as HTML on a webpage. 

```python
def calculate_discounted_price(original_price: float, discount_percentage: float) -> float:
    """
    Calculates the discounted price given the original price and discount percentage.

    :param original_price: The original price of the product.
    :type original_price: float

    :param discount_percentage: The discount percentage to be applied to the original price.
    :type discount_percentage: float

    :return: The discounted price of the product.
    :rtype: float
    """
 
    discounted_price = original_price - ((discount_percentage / 100) * original_price)
    return discounted_price

``` 

## Conclusion
Documenting your code not only helps you write better code and improve code comprehension, but it also helps others understand the code more easily. Providing clear documentation for your code's parameters ensures that anyone using your function will know what type of data to pass to make the function work as expected.
