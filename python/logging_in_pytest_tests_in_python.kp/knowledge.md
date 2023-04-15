---
title: Recording during pytest tests
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Use the `logging` module in Python and configure the logging level to capture logs during your pytest tests.
---

**Contents**

[TOC]

Section 1: Introduction to pytest
pytest is a testing framework in Python that makes it easy to write and run tests. It provides many useful features such as fixtures, parametrized tests, and plugins. In this section, we will briefly introduce pytest and its benefits.

Section 2: Logging in pytest
Logging is an essential part of any testing framework as it helps in debugging and tracking the execution of the test suite. pytest provides a built-in logging feature that can be easily used within test cases. The logging module in Python provides different levels of severity for logging which are DEBUG, INFO, WARNING, ERROR, and CRITICAL.

Section 3: Usage of logging in pytest
To use logging in pytest, you need to import the logging module and create a logger instance. You can then use this logger instance to log messages at different severity levels. In addition, pytest provides the fixture caplog that captures all the logging output during the test execution. The caplog fixture can be used to test the logging messages as well.

Section 4: Conclusion
In conclusion, logging is an essential part of testing and pytest provides an easy way to use logging in test cases. With the built-in logging feature and the caplog fixture, pytest makes it easy to capture and test logging output during the test execution. So next time you are writing tests with pytest, don't forget to include logging!
