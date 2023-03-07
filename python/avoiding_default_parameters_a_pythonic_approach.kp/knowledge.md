---
title: How can one prevent empty lists as default parameters in a pythonic manner?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use `None` as the default parameter value and check if it is None inside the function before creating a new list.
---

**Contents**

[TOC]

## Problem Description

Occasionally, a function's parameter(s) has an assigned default value. When a default value is assigned and changes need to be made to the value, there is risk for potential issues, particularly with mutable types such as a list. 

## Problem Example

```python
def my_function(x, y=[]):
    y.append(x)
    return y

print(my_function(1))  # [1]
print(my_function(2))  # [1, 2]
```

As seen in this example, the initial default list `[]` is created once and, as such, is retained between function calls. A cumulative operation is performed on the list with each function invocation, and hence, the subsequent function calls with a default value affect the previously returned value.

## Pythonic Solution to Avoid Default Parameters that are Empty Lists

### Option 1: Use `None` as a default parameter value

`None` is a safe default value for a parameter that needs to be mutable (like a list). We can then create a new list inside the function using the `if y is None:` statement.

```python
def my_function(x, y=None):
    if y is None:
        y = []
    y.append(x)
    return y

print(my_function(1))  # [1]
print(my_function(2))  # [2]
```

### Option 2: Use a sentinel value for the default parameter

Another approach is to use a unique sentinel value (e.g. a custom string or object) as the default parameter value. We can then check if the parameter is equal to the sentinel value and initialize the default parameter accordingly.

```python
_sentinel = object()

def my_function(x, y=_sentinel):
    if y is _sentinel:
        y = []
    y.append(x)
    return y

print(my_function(1))  # [1]
print(my_function(2))  # [2]
```

### Option 3: Use a decorator

Another way to avoid default parameters that are empty lists is to use a decorator. This decorator checks if the default parameter is a list and replaces it with a new list object whenever the function is called. 

```python
def no_empty_lists(func):
    def wrapper(*args, **kwargs):
        new_args = []
        for arg in args:
            if type(arg) is list and not arg:
                new_args.append([])
            else:
                new_args.append(arg)
        return func(*new_args, **kwargs)
    return wrapper

@no_empty_lists
def my_function(x, y=[]):
    y.append(x)
    return y

print(my_function(1))  # [1]
print(my_function(2))  # [2]
```

### Option 4: Document default parameter behavior

If none of the above methods are suitable, then you should document the behavior of the default parameter. In the function's docstring, document that the default parameter is mutable and that it will be modified if the same default parameter value is used in subsequent calls to the function. 

```python
def my_function(x, y=[]):
    """
    Add x to y and return the result. 
    
    Parameters:
    -----------
    x : int
        The number to add to the list.
    y: list, optional (default=[])
        The list to add x to.
        Note: If y is not supplied, it will be initialized
        to an empty list. If y is supplied and is empty,
        it will be reused in subsequent function calls. 
    """
    y.append(x)
    return y

print(my_function(1))  # [1]
print(my_function(2))  # [1, 2]
```


## Conclusion

It's essential to be mindful of the potential pitfalls of default parameters that are mutable. In Python, we can avoid default parameters that are empty lists by using a sentinel value or using `None` instead of an empty list as the default parameter value. We can also use decorators to check and replace default parameters with a new list object whenever the function is called. Finally, we can inform future code maintainers of the behavior of the default parameter by commenting the function behavior.
