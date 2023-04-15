---
title: Verify that a function or method was not invoked using a mock object
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use assert\_not\_called() function from the mock module to check if a function/method was not called.
---

**Contents**

[TOC]

## Introduction

In Python, you can use the `unittest.mock` module to create mock objects for testing. One common use case for mock objects is to assert that a function or method was not called during a test. In this tutorial, you will learn how to assert a function/method was not called using Mock in Python.

## Creating a Mock Object

To create a mock object in Python, you can use the `unittest.mock.Mock` class. Here's an example:

```python
from unittest.mock import Mock

# Create a mock object
mock_obj = Mock()
```

## Asserting a Function/Method Was Not Called

To assert that a function/method was not called using Mock in Python, you can use the `assert_not_called()` method. Here's an example:

```python
from unittest.mock import Mock

# Create a mock object
mock_obj = Mock()

# Call a function
mock_obj.my_function()

# Assert the function was not called
mock_obj.my_function.assert_not_called()
```

In this example, we create a mock object and call a function on it. We then assert that the function was not called using the `assert_not_called()` method.

## Example

Here's a complete example of how to assert a function/method was not called using Mock in Python:

```python
from unittest.mock import Mock

class MyClass:
    def my_function(self):
        pass

def test_my_function_not_called():
    # Create a mock object
    mock_obj = Mock()

    # Create an instance of MyClass
    my_class = MyClass()

    # Call a function on the mock object
    mock_obj.my_function()

    # Assert the function was not called on the instance of MyClass
    my_class.my_function.assert_not_called()
```

In this example, we create a mock object and an instance of `MyClass`. We then call a function on the mock object and assert that the function was not called on the instance of `MyClass`. This shows how to use Mock to assert that a function/method was not called in Python.

## Conclusion

In this tutorial, you learned how to assert a function/method was not called using Mock in Python. You can create a mock object with `Mock()`, call a function on the mock object, and then use the `assert_not_called()` method to assert that the function was not called.
