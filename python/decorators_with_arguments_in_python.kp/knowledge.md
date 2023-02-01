---
title: What are decorators that take arguments?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Decorators with parameters in Python are functions that accept one or more arguments and return a wrapper function that takes a function as an argument.
---

**Contents**

[TOC]

#### Definition
Decorators with parameters are functions that wrap other functions and take arguments. They are used to modify the behavior of the wrapped function, typically by adding extra functionality.

#### Syntax
The syntax for decorators with parameters is similar to the syntax for regular decorators, but with an additional set of parentheses containing the parameters:

```python
@decorator_with_args(arg1, arg2)
def func(x):
    pass
```

#### Usage
Decorators with parameters can be used to add extra functionality to a function, such as logging, caching, or rate-limiting. For example, the following decorator adds rate-limiting to a function:

```python
from functools import wraps
from time import time

def rate_limited(max_per_second):
    min_interval = 1.0 / float(max_per_second)
    def decorate(func):
        last_time_called = [0.0]
        @wraps(func)
        def rate_limited_function(*args,**kwargs):
            elapsed = time() - last_time_called[0]
            left_to_wait = min_interval - elapsed
            if left_to_wait>0:
                time.sleep(left_to_wait)
            ret = func(*args,**kwargs)
            last_time_called[0] = time()
            return ret
        return rate_limited_function
    return decorate

@rate_limited(2) # two per second at most
def print_num(num):
    print(num)
```

#### Conclusion
Decorators with parameters can be used to add extra functionality to functions. They are a powerful tool for modifying the behavior of functions without changing their source code.
