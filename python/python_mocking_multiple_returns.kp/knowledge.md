---
title: Create multiple return values in Python using mocking
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: In Python, multiple return values can be simulated by packing the values into a tuple and returning the tuple.
---

**Contents**

[TOC]

# Section 1: Introduction

Python's mock library provides a powerful set of tools for testing code that uses external services or resources. It allows developers to create mock objects that simulate the behavior of the external services or resources in a controlled environment. One of the features of the mock library is the ability to return multiple values from a single call. This can be useful when testing complex logic that requires multiple values to be returned from a single call.

# Section 2: How to Mock Multiple Return Values

Mocking multiple return values is done by creating a mock object and then setting the return_value attribute to a tuple of the desired values. The mock object can then be used in place of the external service or resource, and the values in the tuple will be returned in the same order as they were specified.

For example, if a function needs to return two values, a string and an integer, the mock object can be set up as follows:

mock_object = mock.Mock()
mock_object.return_value = ("string value", 42)

# Section 3: Examples

Here are a few examples of how to use the mock library to return multiple values.

Example 1:

def some_function():
    return mock_object()

mock_object = mock.Mock()
mock_object.return_value = ("string value", 42)

result = some_function()
print(result) # prints ("string value", 42)

Example 2:

def some_other_function():
    return mock_object()

mock_object = mock.Mock()
mock_object.return_value = (True, "hello world")

result = some_other_function()
print(result) # prints (True, "hello world")

# Section 4: Conclusion

Mocking multiple return values is a powerful tool for testing code that requires multiple values from a single call. It allows developers to create mock objects that simulate the behavior of the external services or resources in a controlled environment, and return the desired values in the same order as specified.
