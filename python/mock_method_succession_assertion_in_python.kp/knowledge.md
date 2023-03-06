---
title: Claiming that a mock method is being called repeatedly
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can assert successive calls to a mock method in Python using the assert\_called\_once\_with() and assert\_has\_calls() methods.
---

**Contents**

[TOC]

Section 1: Introduction to Mocking in Python
Mocking is a technique for testing code by simulating the behavior of specific components or dependencies. Python provides a built-in library called unittest.mock, which facilitates mocking in Python.

Section 2: Asserting Successive Calls to a Mock Method
Mock objects allow us to simulate (and assert the behavior of) a method call multiple times with different arguments. To do this, we first create a mock object with the desired method, then we set a return value, and finally, we make multiple calls to the method with different input arguments.

For example:

```
from unittest.mock import Mock

# Create a mock object
mock_obj = Mock()

# Set the return value of the mocked method
mock_obj.some_method.return_value = "Mocked Value"

# Call the mocked method multiple times with different input arguments
assert mock_obj.some_method("input1") == "Mocked Value"
assert mock_obj.some_method("input2") == "Mocked Value"
assert mock_obj.some_method("input3") == "Mocked Value"
```

Section 3: Asserting Successive Calls with Different Return Values
We can also simulate the behavior of the mocked method by returning different values based on the input arguments. We can set this behavior using the side_effect attribute of the mock object.

For example:

```
from unittest.mock import Mock

# Create a mock object
mock_obj = Mock()

# Define the behavior of the mocked method
mock_obj.some_method.side_effect = ["value1", "value2", "value3"]

# Call the mocked method multiple times with different input arguments
assert mock_obj.some_method("input1") == "value1"
assert mock_obj.some_method("input2") == "value2"
assert mock_obj.some_method("input3") == "value3"
```

Section 4: Conclusion
Mocking is a powerful technique for testing code behavior without relying on external dependencies. In Python, we can use the built-in unittest.mock library to create mock objects and simulate the behavior of specific components or dependencies. By setting the return value or side_effect of a mocked method, we can simulate the behavior of the method call multiple times with different input arguments.
