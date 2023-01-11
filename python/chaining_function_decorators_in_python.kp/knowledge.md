---
title: What is the process of creating and linking multiple function decorators?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-11 00:00:00
updated_at: 2023-01-11 00:00:00
tldr: You can use the @ symbol to decorate functions, and can chain them together by nesting them one inside the other.
---

**Contents**

[TOC]

### Creating a Function Decorator

A function decorator is a special type of function that takes another function as an argument and adds some additional functionality to it. To create a function decorator, you need to define a function that takes a function as an argument and returns a new function that wraps the original function.

For example, the following decorator adds a logging message to a function:

```python
def log_function(func):
    def wrapper(*args, **kwargs):
        print(f"Function {func.`__name__`} called with args {args} and kwargs {kwargs}")
        return func(*args, **kwargs)
    return wrapper
```

### Chaining Decorators

Decorators can be chained together to add multiple layers of functionality to a function. To do this, you need to apply the decorators in reverse order, starting with the innermost decorator and working outwards.

For example, the following code creates two decorators and chains them together to add logging and timing functionality to a function:

```python
def log_function(func):
    def wrapper(*args, **kwargs):
        print(f"Function {func.`__name__`} called with args {args} and kwargs {kwargs}")
        return func(*args, **kwargs)
    return wrapper

def time_function(func):
    def wrapper(*args, **kwargs):
        start_time = time.time()
        result = func(*args, **kwargs)
        end_time = time.time()
        print(f"Function {func.`__name__`} took {end_time - start_time} seconds to execute")
        return result
    return wrapper

@time_function
@log_function
def add(a, b):
    return a + b
```

### Using Decorators

Once you have created a function decorator, you can use it to wrap any function you want. To do this, you need to use the `@` symbol before the decorator name when defining the function.

For example, the following code uses the `log_function` decorator to wrap the `add` function:

```python
@log_function
def add(a, b):
    return a + b
```

### Conclusion

Function decorators are a powerful tool for adding additional functionality to functions in Python. They can be chained together to add multiple layers of functionality, and they can be used to wrap any function you want.
