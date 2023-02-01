---
title: What is the correct way to verify that an exception is being raised in pytest?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Assert that the expected exception is raised using the pytest.raises() context manager.
---

**Contents**

[TOC]

## Section 1: Importing the Required Libraries

In order to use pytest to assert that an exception gets raised, it is necessary to import two libraries: `pytest` and `pytest-raises`. 

`pytest` is the main library that allows you to write tests for your code.

`pytest-raises` is an additional library that provides a decorator for asserting that an exception is raised when running a test.

The code for importing these libraries would look like this:

```python
import pytest
from pytest_raises import raises
```

## Section 2: Writing the Test

Once the necessary libraries have been imported, you can write a test to assert that an exception gets raised. The code for this test would look something like this:

```python
@raises(ValueError)
def test_exception():
    raise ValueError
```

This test uses the `@raises` decorator to specify the type of exception that is expected to be raised. In this case, the test is expecting a `ValueError` to be raised. 

## Section 3: Running the Test

Once the test has been written, it can be run using the `pytest` command. This command will run the test and check to see if the expected exception is raised.

If the exception is raised, the test will pass and the output will look something like this:

```
============================= test session starts =============================
platform darwin -- Python 3.6.9, pytest-5.4.3, py-1.9.0, pluggy-0.13.1
rootdir: /Users/username/tests
collected 1 item                                                              

test_exception.py .                                                       [100%]

============================== 1 passed in 0.01s ==============================
```

If the exception is not raised, the test will fail and the output will look something like this:

```
============================= test session starts =============================
platform darwin -- Python 3.6.9, pytest-5.4.3, py-1.9.0, pluggy-0.13.1
rootdir: /Users/username/tests
collected 1 item                                                              

test_exception.py F                                                       [100%]

================================= FAILURES ===================================
___________________________ test_exception ___________________________________

@raises(ValueError)
def test_exception():
    >   raise ValueError
E   ValueError

test_exception.py:3: ValueError
============================== 1 failed in 0.01s ==============================
```

## Section 4: Conclusion

In conclusion, pytest can be used to assert that an exception gets raised by writing a test and using the `@raises` decorator to specify the type of exception that is expected to be raised. The test can then be run using the `pytest` command to check if the expected exception was raised.
