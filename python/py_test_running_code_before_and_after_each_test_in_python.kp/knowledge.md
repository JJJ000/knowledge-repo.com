---
title: Could you rewrite the statement "run code before and after each test in py.test?"
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: To run code before each test, you can use the pytest fixture `setup\_function()`, and to run code after each test, you can use the pytest fixture `teardown\_function()`.
---

**Contents**

[TOC]

# Introduction

`pytest` is a unit testing framework that provides a rich featureset for testing Python code. Like any other testing framework, it comes with a handful of hooks that allow you to perform some actions before and after each test. In this article, we are going to see how to run code before and after each `pytest` test in Python.

# Pytest Hooks

`pytest` framework has a variety of hooks that run at different times during test execution. A hook is a function with a specific name and signature that pytest invokes at the correct time during a test run. Here are some of the most commonly used hooks in `pytest`:

- `pytest_runtest_setup`: called before invoking each test function.
- `pytest_runtest_call`: called to execute the test function.
- `pytest_runtest_teardown`: called after a test function has finished being executed.

Each of these hooks is provided with an argument `item`, which is a `pytest.Item` object representing the test item being run. You can access the test name, filename, test function, and other details from this object.

# Running Code Before Each Test

To run code before each test in `pytest`, we can use the `pytest_runtest_setup` hook. Here's an example:

```python
# conftest.py

def pytest_runtest_setup(item):
    print("Running setup for:", item.name)
    # add your setup code here
```

In this example, we are defining the `pytest_runtest_setup` hook in a `conftest.py` file. This file is automatically discovered by pytest and contains any fixtures or hooks that need to be shared across multiple test files.

When this hook is invoked, it will print the name of the test being run and execute any setup code you add in its body. Keep in mind that this hook is executed before invoking each test function, so any code placed in this hook will be run multiple times.

# Running Code After Each Test

To run code after each test in `pytest`, we can use the `pytest_runtest_teardown` hook. Here's an example:

```python
# conftest.py

def pytest_runtest_teardown(item):
    print("Running teardown for:", item.name)
    # add your teardown code here
```

In this example, we are defining the `pytest_runtest_teardown` hook in a `conftest.py` file. This hook is executed after each test function has finished running.

Like the `pytest_runtest_setup` hook, this hook is executed multiple times, once for each test function, so any code placed in this hook will also be run multiple times. You can use this hook to do things like closing resources, cleaning up data, or performing any other necessary teardown activities.

# Conclusion

`pytest` provides a wide range of hooks that can be used to customize the test execution process. In this article, we've seen how to use the `pytest_runtest_setup` and `pytest_runtest_teardown` hooks to run code before and after each test. These hooks can be used to perform any necessary setup or teardown activities to ensure that your tests run smoothly and consistently.
