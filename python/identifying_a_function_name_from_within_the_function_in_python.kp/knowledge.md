---
title: Find the name of the function within the function without using traceback
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The function name can be determined by using the `inspect` module and calling the `stack()` function, which will return the current stack frame.
---

**Contents**

[TOC]

# Section 1: How to Determine a Function Name

In Python, the function name can be determined by using the keyword 'def' followed by the function name. For example, for the function below:

```
def my_function():
    return "Hello World!"
```

The function name is 'my_function'.

# Section 2: Using the inspect Module

The inspect module can also be used to determine the function name. For example, the following code can be used to determine the function name of the above function:

```
import inspect

def my_function():
    return "Hello World!"

print(inspect.currentframe().f_code.co_name)
```

The output of this code will be 'my_function'.

# Section 3: Using the __name__ Attribute

The __name__ attribute can be used to determine the function name. For example, the following code can be used to determine the function name of the above function:

```
def my_function():
    return "Hello World!"

print(my_function.__name__)
```

The output of this code will be 'my_function'.

# Section 4: Using the __qualname__ Attribute

The __qualname__ attribute can also be used to determine the function name. For example, the following code can be used to determine the function name of the above function:

```
def my_function():
    return "Hello World!"

print(my_function.__qualname__)
```

The output of this code will be 'my_function'.
