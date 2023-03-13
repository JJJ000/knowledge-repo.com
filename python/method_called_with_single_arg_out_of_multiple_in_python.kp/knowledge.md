---
title: Confirm that a method has been invoked using a single argument from a group of multiple arguments
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: You can use the `assert\_called\_once\_with` method from the unittest module to check that a method was called with a specific argument in Python.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, unit testing involves testing the individual components of a software system to ensure that they are performing their intended functions. When writing unit tests, it is common to want to assert that a particular method was called with a specific argument out of several possible ones. 

Section 2: Using assert_called_with
Python provides a built-in method called `assert_called_with` that allows us to assert that a method was called with specific arguments. This method is part of the `unittest.mock` library and can be used as follows:

```python
from unittest.mock import Mock

# Create a mock object
my_mock = Mock()

# Call a method on the mock object
my_mock.my_method(1, 2, 3)

# Assert that the method was called with the second argument equal to 2
my_mock.my_method.assert_called_with(1, 2, 3)

# Assert that the method was called with the third argument equal to 3
my_mock.my_method.assert_called_with(1, 3, 3) # Will cause the test to fail!
```

In this example, we create a mock object and call the `my_method` method with three arguments. We then use `assert_called_with` to ensure that the method was called with the correct arguments.

Section 3: Using side_effect
Another way to assert that a method was called with a specific argument is to use the `side_effect` attribute of a mock object. This attribute allows us to specify a function to be called when the method is called, and we can use this function to perform the assertion.

```python
from unittest.mock import Mock

def my_side_effect(*args):
    assert args[1] == 2
    return None

# Create a mock object with a side effect
my_mock = Mock(side_effect=my_side_effect)

# Call the method on the mock object and assert that it was called with the second argument equal to 2
my_mock.my_method(1, 2, 3)
```

In this example, we define a function called `my_side_effect` that asserts that the second argument is equal to 2. We then create a mock object with this side effect and call the `my_method` method with three arguments. The side effect function is called with these arguments and performs the assertion.

Section 4: Conclusion
In conclusion, there are several approaches we can take to assert that a method was called with one argument out of several in Python. We can use `assert_called_with` to check the arguments that were passed to the method, or we can use the `side_effect` attribute of a mock object to perform the assertion. Both of these approaches can be useful in different testing scenarios.
