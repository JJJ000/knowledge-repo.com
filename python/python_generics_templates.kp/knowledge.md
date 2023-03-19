---
title: Can you rephrase the term 'generics/templates in python'?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Python supports templates through the use of TypeVar and Generic classes in the typing module.
---

**Contents**

[TOC]

Introduction

Python doesn't have a generic/template keyword like in other programming languages such as Java or C++. However, there are ways to achieve similar functionality in Python.

Section 1: Type hints with TypeVar

TypeVar is a class in the typing module that can be used to declare a generic type variable. This allows functions, classes, and methods to work with different types while still enforcing type hints.

For example, the following code declares a generic function that takes two arguments of any type T and returns a tuple of type T:

```
from typing import TypeVar, Tuple

T = TypeVar('T')

def pair(a: T, b: T) -> Tuple[T, T]:
    return a, b
```

In this example, the TypeVar class is used to declare a generic variable T. This variable is then used as the type hint for the function arguments and return value.

Section 2: Inheritance with Generics

Python also allows inheritance with generics. This allows derived classes to inherit the generic types and methods of their base classes.

For example, the following code creates a generic Stack class using inheritance:

```
from typing import TypeVar, Generic

T = TypeVar('T')

class Stack(Generic[T]):
    def __init__(self):
        self.items = []

    def push(self, item: T) -> None:
        self.items.append(item)

    def pop(self) -> T:
        return self.items.pop()
```

In this example, the Stack class inherits from the Generic class while also declaring a generic type variable T. This allows the push and pop methods to work with any type T.

Section 3: Using Any and Union

Another approach for achieving similar functionality to generics in Python is using the Any keyword or the Union class in the typing module.

The Any keyword can be used to indicate that a variable or argument can be any type. For example:

```
def echo(arg: Any) -> Any:
    return arg
```

In this example, the argument and return value can be any type, as indicated by the Any keyword.

The Union class allows multiple types to be specified for a single argument or variable. For example:

```
from typing import Union

def add(a: Union[int, float], b: Union[int, float]) -> Union[int, float]:
    return a + b
```

In this example, the add function can take two arguments of either the int or float type, and the return value can be either int or float.

Conclusion

While Python doesn't have a generic/template keyword, there are still ways to achieve similar functionality using type hints with TypeVar, inheritance with generics, and the Any keyword or Union class. These features allow Python to be a flexible and dynamic language while still providing type hints and type safety.
