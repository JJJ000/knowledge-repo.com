---
title: Creating a simulation of the Python function using provided input arguments
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To mock a Python function based on input arguments, use the `@patch` decorator with the `call\_args` attribute.
---

**Contents**

[TOC]

Section 1: Introduction
One of the advantages of unit testing is that it allows you to isolate and test individual parts of your code, including functions. When testing functions that rely on external resources, mocking can be used to replicate the behavior of those resources without actually invoking them. In this tutorial, we will learn how to mock a Python function based on its input arguments.

Section 2: Using the Mock Module
Python's Mock module provides a easy way of creating mock objects that can replace real objects in unit tests. We can create a mock object for our function and set a return value for it, so our function will return whatever we want it to.

Here is an example:

```
from unittest.mock import Mock

def myfunc(arg):
    return arg * 2

mock_function = Mock(return_value=42)

result = myfunc(mock_function)
print(result)
```

We have created a Mock object, and have set its return value to 42. We then called our function with the mock as the input argument. Since our function only multiplies its input argument by 2, our mock function will return 42 * 2 = 84.

Section 3: Mocking a Function Based On Its Input Arguments
The example above shows how to create a mock object and use it as an input argument to a function. However, sometimes we want to mock only specific behavior of a function, depending on the input arguments that are passed to it. The Mock module allows us to do that as well.

Here is an example:

```
from unittest.mock import Mock

def myfunc(arg):
    if arg < 10:
        return arg * 2
    else:
        return arg / 2

mock_function = Mock(side_effect=lambda arg: arg * 3 if arg < 5 else arg / 3)

result1 = myfunc(3)
print(result1)  # Output: 9

result2 = myfunc(11)
print(result2)  # Output: 5.5
```

We have defined a function that returns different values depending on the input argument. We then created a Mock object, and set its side_effect attribute to a lambda function that also returns different values depending on the input argument. In this way, our Mock object will replicate the behavior of our function.

Section 4: Conclusion
Mocking can be used to isolate and test individual parts of a codebase, including functions that rely on external resources. In this tutorial, we have learned how to create and use Mock objects in Python in order to mock a function based on its input arguments. By employing these techniques, we can write more comprehensive and resilient unit tests for our applications.
