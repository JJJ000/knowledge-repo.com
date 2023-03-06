---
title: Provide an argument to a fixture function
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can pass a parameter to a fixture function in Python by decorating the test function with a pytest.mark.parametrize annotation that specifies the parameter value.
---

**Contents**

[TOC]

Section 1: Introduction

In Pytest, a fixture is a reusable block of code that can be used to set up a test environment. These fixtures are created using fixture functions, which are executed before the test functions.

Sometimes, we need to pass a parameter to a fixture function in order to customize the test environment. In this article, we will discuss how to pass a parameter to a fixture function in Python.

Section 2: Passing a parameter to a fixture function

To pass a parameter to a fixture function, we can use the `request` object that is available inside the fixture function. The `request` object provides access to the test context and can be used to get information about the current test.

Here's an example of how to pass a parameter to a fixture function:

```python
import pytest

@pytest.fixture
def my_fixture(request, my_param):
    print(f"Running my_fixture with param {my_param}")
    # do some setup
    yield
    # do some teardown

def test_function(my_fixture):
    # test something
    pass
```

In this example, we define a fixture function called `my_fixture`, which takes two parameters: `request` and `my_param`. The `request` parameter is provided automatically by Pytest and is used to get information about the test. The `my_param` parameter is the parameter that we want to pass to the fixture function.

We then define a test function called `test_function`, which uses the `my_fixture` fixture.

To pass a value to the `my_param` parameter, we can use the `pytest.fixture` decorator with a `params` argument. Here's how:

```python
@pytest.fixture(params=[1, 2, 3])
def my_param(request):
    return request.param

def test_function(my_param):
    assert my_param > 0
```

In this example, we define a fixture function called `my_param`, which takes a `request` parameter. We use the `params` argument of the `pytest.fixture` decorator to specify a list of values that we want to pass to the fixture function. The `request.param` attribute is used to access the value that is passed to the fixture function.

The `test_function` uses the `my_param` fixture, which will be executed three times, once for each value in the list.

Section 3: Using fixtures with classes

We can also use fixtures with test classes. In this case, the fixture functions will be executed once per class, not once per test method.

Here's an example of how to use fixtures with test classes:

```python
@pytest.fixture
def my_fixture(request, my_param):
    print(f"Running my_fixture with param {my_param}")
    # do some setup
    yield
    # do some teardown

@pytest.mark.usefixtures("my_fixture")
class TestClass:
    def test_method1(self):
        # test something
        pass

    def test_method2(self):
        # test something else
        pass
```

In this example, we define a fixture function called `my_fixture`, which takes two parameters: `request` and `my_param`.

We then define a test class called `TestClass`, which uses the `@pytest.mark.usefixtures("my_fixture")` decorator to use the `my_fixture` fixture for all test methods in the class.

Section 4: Conclusion

Passing a parameter to a fixture function in Python is easy using the `request` object and the `pytest.fixture` decorator with the `params` argument. We can also use fixtures with test classes by using the `@pytest.mark.usefixtures` decorator. These techniques allow us to customize the test environment and make our tests more flexible and powerful.
