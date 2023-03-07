---
title: Py.test can be used to log test execution times and identify slow tests
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To print test execution times and pinpoint slow tests with py.test in Python, use the --durations and --timeout options respectively.
---

**Contents**

[TOC]

## Introduction
Test execution time is an essential metric to evaluate the performance of a test suite. It helps developers to pinpoint slow-running tests that can affect the overall speed of the test execution process. Py.test is a popular testing framework in Python that provides several ways to measure and report test execution time. In this article, we will explore how to print test execution times and identify slow tests using py.test.


## 1. Printing Test Execution Times
Py.test provides various built-in options to print test execution times. One of the easiest ways to get the execution time is to use the `--durations` option. It displays the N slowest tests, their duration time, and other information like the name of the test function, file name, and line number. Here is an example command to run tests with `--durations` flag:

```bash
$ pytest --durations=10
```
It will display the 10 slowest tests in descending order of execution time. If we want to print the execution time of all tests at the end of the test run, use the `--durations=0` option. It will print the list of all tests with their execution times.

```bash
$ pytest --durations=0
```
This command will output something like:

```
============================================ test session starts =============================================
platform linux -- Python 3.x.x, pytest-6.x.x, py-1.x.x, pluggy-1.x.x
rootdir: /path/to/project
plugins: cov-2.x.x, flask-1.x.x
collected 10 items

test_module1.py ...........                                                                    [100%]

========================================= slowest test durations ==========================================
0.26s call     test_module1.py::test_slow_test
0.15s call     test_module1.py::test_another_slow_test
0.10s call     test_module2.py::test_slow_test2
0.05s call     test_module3.py::test_slow_test3
0.03s call     test_module1.py::test_fast_test1
0.02s call     test_module2.py::test_fast_test2
0.01s call     test_module2.py::test_fast_test3
0.01s call     test_module3.py::test_fast_test4
0.01s call     test_module3.py::test_fast_test5
0.00s call     test_module1.py::test_fast_test2

========================================= 10 passed in 0.98s ==========================================
```
In this output, we can see that the slowest test `test_slow_test` took 0.26 seconds to run. By using the `--durations` flag, we can easily identify the slowest tests and optimize them.


## 2. Pinning Down Slow Tests
Once we have identified the slowest tests, we need to analyze their performance and check whether we can optimize them. Py.test provides several ways to run the tests with profiling to identify the root cause of slow running tests. One way to do that is by using the `--profile` flag.

```bash
$ pytest --profile
```
It will enable profiling for all tests and output the profiling report for each test in a separate file. The report includes the number of function calls for each function, the time spent inside the function, and the time spent in the function's subroutines. By analyzing the profiling report, we can find out which function is taking more time inside the slowest test and optimize it.

Another way to identify slow running tests is by using the `--trace` flag. It prints a stack trace whenever a test takes more than the specified time. For example, if we want to trace tests that take more than 500 milliseconds, use the following command:

```bash
$ pytest --trace --durations=0 --max-time=0.5
```
It will print a stack trace whenever a test takes more than 500 milliseconds to complete. By analyzing the stack trace, we can pinpoint the root cause of slow running tests and optimize them.


## Conclusion
In this article, we learned how to print test execution times and identify slow tests using py.test. Py.test provides various built-in options like `--durations`, `--profile`, and `--trace` that help us analyze the test suite's performance and optimize it. By identifying and optimizing slow running tests, we can speed up the test execution process and improve the development workflow.
