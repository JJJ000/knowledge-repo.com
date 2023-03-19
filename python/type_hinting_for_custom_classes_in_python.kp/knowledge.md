---
title: Using user-defined classes in type hints
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Type hints can be applied to user-defined classes in Python to provide better readability and maintainability of the code.
---

**Contents**

[TOC]

Section 1: Introduction
Type hints are a way to specify the type of a variable or function argument in Python. This can be useful for improving code readability, catching errors early, and making code easier to understand.

Section 2: Basic type hints
Python supports basic type hints for built-in types such as integers, strings, and lists. For example, the following function uses type hints for two arguments, a list and an integer:

```python
def get_item(lst: List[str], index: int) -> str:
    return lst[index]
```

This function takes a list of strings and an integer index, and returns the string at the specified index.

Section 3: Type hints with user-defined classes
Python also supports type hints for user-defined classes. To do this, you can import the class and use it as the type hint. For example:

```python
from my_module import MyClass

def do_something(x: MyClass) -> None:
    # code goes here
```

This function takes an instance of the MyClass class as an argument and returns nothing.

Section 4: Union types
If you want to allow multiple types for an argument, you can use a union type. For example:

```python
from typing import Union

def my_function(x: Union[int, str]) -> None:
    # code goes here
```

This function takes an argument that can be either an integer or a string, and returns nothing.
