---
title: What makes an empty dictionary a risky default value in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: The empty dictionary is a dangerous default value in Python because it is mutable and can lead to unintended changes in the function`s behavior.
---

**Contents**

[TOC]

## 1. The concept of default arguments
In Python, we can define a function with default arguments. When we call the function and we omit such an argument, Python will automatically substitute the default value. This is a useful feature because it saves us from having to specify every argument all the time.

## 2. The problem with mutable default values
However, when we use a mutable object as the default value, we create a subtle bug that can lead to unexpected behavior. Since the default value is evaluated only once at the time of function definition, all calls to the function will share the same object instance.

## 3. A dictionary example
Consider a function that takes a dictionary as an optional argument. We could define it like this:

``` python
def foo(d={}):
    d['foo'] = 42
    return d
```

This function will add a key-value pair to the input dictionary, or create one if no argument was passed. If we call the function multiple times without an argument, we might expect to get separate dictionaries with only one key-value pair each. However, this is not what happens:

``` python
>>> foo()
{'foo': 42}
>>> foo()
{'foo': 42, 'foofoo': 42}
>>> foo()
{'foo': 42, 'foofoo': 42, 'foofoofoo': 42}
```

We get a dictionary with more and more keys every time we call the function, because `d` is always the same object that gets modified over and over again.

## 4. Conclusion
In conclusion, the empty dictionary is a dangerous default value in Python because it is mutable and gets shared among all calls to the function. To avoid this issue, we can use `None` as the default value and create a new dictionary inside the function if the argument is `None`. Alternatively, we can use immutable objects like tuples, integers, or strings as default values.
