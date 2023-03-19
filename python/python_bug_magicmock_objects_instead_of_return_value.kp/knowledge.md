---
title: Instead of returning a return_value, Python produces a magicmock object
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: This happens because the MagicMock object is returned when a method or attribute is accessed on a Mock object, and no return value has been specifically set using the return\_value attribute.
---

**Contents**

[TOC]

### Introduction
The `MagicMock` object is a class from the `unittest.mock` module in Python that is often used for testing purposes. It can mock functions, classes or objects and has many features like tracking how it is called, controlling its behaviour, and so on. However, sometimes when using the `MagicMock` object, we might encounter an unexpected behaviour where it returns an instance of the `MagicMock` object instead of the expected return value. In this article, we will discuss some common reasons why this might happen and how to solve them.

### Reason 1: Incorrect Mocking
One common reason why the `MagicMock` object returns an instance of itself instead of the expected return value is due to incorrect mocking. When we use the `MagicMock` to mock a function or method, we need to make sure that we set the `return_value` attribute of the `MagicMock` object to the expected return value. If we forget to set this attribute or set it incorrectly, the mocked function or method might return a `MagicMock` instead of the intended return value. 

```python
from unittest.mock import MagicMock

# Incorrect mocking
def my_function():
    return "hello"

my_mock = MagicMock()
my_mock(my_function()) # returns a MagicMock object
```

To solve this issue, we need to make sure that we set `return_value` attribute of `my_mock` to the expected return value. 

```python
# Correct mocking
my_mock = MagicMock()
my_mock.return_value = "hello"
my_mock(my_function()) # returns "hello"
```

### Reason 2: Non-Existent Attribute
Another reason why the `MagicMock` object might return itself instead of the expected return value is if we try to access a non-existent attribute of the `MagicMock` object. When we access a non-existent attribute of the `MagicMock` object, by default it returns another `MagicMock` object. 

```python
my_mock = MagicMock()
my_mock.nonexistent_attribute # returns a MagicMock object
```

To avoid this behaviour, we can set the `spec` attribute of the `MagicMock` to the class or object that we want to mock. This will ensure that any non-existent attributes will raise an `AttributeError` instead of returning another `MagicMock` object.

```python
my_mock = MagicMock(spec=my_class)
my_mock.nonexistent_attribute # raises AttributeError
```

### Reason 3: Multiple `MagicMock` Objects
The third reason why we might encounter this issue is if we have multiple `MagicMock` objects chained together. When we chain multiple `MagicMock` objects, the last `MagicMock` object in the chain is the one that returns the final value. If we forget to set the `return_value` attribute on the last `MagicMock` object, it will use the default behaviour and return another `MagicMock` object.

```python
my_mock1 = MagicMock()
my_mock2 = MagicMock()
my_mock1.return_value = my_mock2
# Will return a MagicMock object instead of True
my_mock2.should_return_true()
```

To solve this issue, we need to make sure that we set the `return_value` attribute of the last `MagicMock` object in the chain to the expected return value.

```python
my_mock1 = MagicMock()
my_mock2 = MagicMock()
my_mock1.return_value = my_mock2
my_mock2.should_return_true.return_value = True
# Will return True
my_mock2.should_return_true()
```

### Conclusion
In conclusion, when encountering an issue where the `MagicMock` object returns itself instead of the expected return value, we should check if we have correctly set the `return_value` attribute, if we are accessing a non-existent attribute, or if we have multiple `MagicMock` objects chained together. By following these guidelines, we can ensure that our mocked functions and methods behave as expected.
