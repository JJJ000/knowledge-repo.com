---
title: What is the method for determining the return type and argument types of a function?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use Python`s built-in `type()` function to get the return type of a function, and the `inspect` module`s `signature()` function to get the argument types.
---

**Contents**

[TOC]

## Using the `type()` function

The `type()` function is a built-in function in Python that returns the type of an object. We can use it to find the return type of a function. 

### Example
```
def add(a, b):
    return a + b

result = add(2, 3)
print(type(result)) # <class 'int'>
```

In the above code, we define the function `add()` that takes two arguments `a` and `b` and returns their sum. We then call the function with arguments 2 and 3, and assign the result to a variable `result`. Finally, we use the `type()` function to print the type of `result`, which is an `int`.

## Using the `inspect` module

The `inspect` module provides several functions for inspecting live objects in a program. We can use the `signature()` function in the `inspect` module to get information about a function's arguments.

### Example
```
import inspect

def greet(name: str) -> str:
    return f"Hello, {name}!"

print(inspect.signature(greet)) # (name: str) -> str
```

In the above code, we define the function `greet()` that takes one argument `name` of type `str` and returns a string. We then use the `signature()` function from the `inspect` module to print the function's signature, which includes the argument types and the return type.

## Using type annotations

Python 3 introduced support for type annotations, which allow us to annotate function and variable declarations with type information. We can use this feature to explicitly specify the argument types and return types of a function.

### Example
```
def multiply(a: int, b: int) -> int:
    return a * b

result = multiply(3, 4)
print(result) # 12
```

In the above code, we define the function `multiply()` that takes two arguments of type `int` and returns their product as an `int`. We then call the function with arguments 3 and 4, and assign the result to a variable `result`. Finally, we print the value of `result`.

## Using IDEs or code editors with IntelliSense

Many IDEs and code editors provide IntelliSense functionality, which can automatically detect and display the argument types and return type of a function. This can be particularly useful for exploring new libraries or APIs.

### Example (using VS Code)
```
def divide(a: float, b: float) -> float:
    return a / b

result = divide(6, 2)
```

In the above code, we define the function `divide()` that takes two arguments of type `float` and returns their quotient as a `float`. In VS Code, if we type `divide(` and wait for a moment, the editor will display a tooltip with information about the function's arguments and return type.

Note that not all code editors or IDEs support this feature, and it may require additional setup or configuration.
