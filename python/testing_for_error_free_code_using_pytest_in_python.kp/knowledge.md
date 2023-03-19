---
title: What is the way to utilize pytest for verifying the non-occurrence of an error?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To check that Error is NOT raised in Python using pytest, use the assert statement with the `not` keyword and the `raises` method, like so assert not pytest.raises(Error) function\_call().
---

**Contents**

[TOC]

## Installing pytest

First, you need to ensure that pytest is installed on your system. To install pytest, simply run the following command:

```
pip install pytest
```

This will install pytest on your system, and you'll be ready to start using it for your Python projects.

## Writing a Test Function

Next, you'll need to write a test function. A test function is a function that tests a specific part of your code to ensure that it works as expected. Here's an example of a test function that tests whether a specific function raises an error:

```python
def test_no_error_raised():
    try:
        # Call your function here
    except Exception:
        # Raise an error if an exception is thrown
        assert False
    else:
        # Assert that no error was raised
        assert True
```

## Running the Tests

Once you have a test function, you can run it using pytest. To run a test function, you simply need to run the `pytest` command followed by the name of the file containing your test function:

```
pytest test_file.py
```

This will run your test function and output the results to the console. If everything passes, you'll see a message like this:

```
=========================== test session starts ============================
collecting ... collected 1 item

test_file.py .                                                       [100%]

========================= 1 passed in 0.01 seconds =========================
```

On the other hand, if an error is raised during the test, you'll see an error message like this:

```
=========================== test session starts ============================
collecting ... collected 1 item

test_file.py F                                                       [100%]

================================= FAILURES =================================
___________________________ test_no_error_raised ___________________________

    def test_no_error_raised():
        try:
            # Call your function here
        except Exception:
            # Raise an error if an exception is thrown
>           assert False
E           assert False

test_file.py:6: AssertionError
========================= 1 failed in 0.01 seconds =========================
```

## Conclusion

In conclusion, using pytest to check that an error is not raised in Python is easy. First, you need to ensure that pytest is installed on your system. Next, you'll need to write a test function that tests whether your function raises an exception. Finally, you can run your tests using the `pytest` command and see the test results in the console. With this approach, you can ensure that your code works as expected and that no errors are raised.
