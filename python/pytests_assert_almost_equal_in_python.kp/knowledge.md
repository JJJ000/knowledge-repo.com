---
title: Asserting near equality in pytest
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: The pytest.approx() method can be used to assert almost equal values in Python.
---

**Contents**

[TOC]

Section 1: Introduction to pytest

Pytest is a popular testing framework in Python. It provides an extensive set of features to make testing easier, faster, and more productive. Pytest supports various types of assertions that allow developers to test their code for correctness. 

Section 2: Assertion in pytest

One of the most commonly used assertions in pytest is assert. It checks whether the given expression is true or false. The assert statement takes a single argument, which is a Boolean expression. If the expression is true, then the program proceeds; otherwise, it raises an AssertionError with an optional message.

assert expression, message

Section 3: Almost equal assertion in pytest

To check if two floating-point numbers are equal, or almost equal, pytest provides an almost equal assertion. The pytest.approx() method compares two values with a given tolerance, allowing for a small range of difference between the values. 

For example, assume we want to test if the result of the following computation is almost equal to 0.3:

def test_almost_equal():
    a = 0.1 + 0.1 + 0.1
    assert a == 0.3

In this case, the test will fail because a is not exactly equal to 0.3 due to floating-point precision. To make the test pass, we can change the assertion to use pytest.approx() as follows:

def test_almost_equal():
    a = 0.1 + 0.1 + 0.1
    assert a == pytest.approx(0.3)

Section 4: Tolerance with almost equal assertion

The pytest.approx() method allows the developer to specify a tolerance value, which is used to compare the two values. The tolerance can be specified by either an absolute or relative error value.

To specify a relative error value, we can set rel=value, where the value is the relative tolerance. To specify an absolute error value, we can set abs=value, where the value is the absolute tolerance. If both are given, then the comparison uses the maximum of the two tolerances.

For example, let's say we want to test if the result of dividing two floating-point numbers is almost equal to 2 with an absolute tolerance of 0.1. We can write the assertion as follows:

def test_division():
    a = 5.0
    b = 2.5
    assert a/b == pytest.approx(2, abs=0.1)

This assertion will pass because a/b is almost equal to 2 with an absolute tolerance of 0.1. 

Conclusion:

In conclusion, pytest provides a variety of assertions to test the code's correctness. When comparing floating-point numbers, we could use pytest.approx() assertion to allow for slight differences between the values, providing a tolerance value.
