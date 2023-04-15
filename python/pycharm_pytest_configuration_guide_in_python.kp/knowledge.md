---
title: What are the steps to set up pycharm for running py.test tests?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To configure PyCharm to run py.test tests in Python, go to `Run` -> `Edit Configurations` -> `Add New Configuration` and select `py.test` as the test runner.
---

**Contents**

[TOC]

# Configuring PyCharm for py.test Tests in Python

PyCharm is an excellent IDE for Python developers with lots of features that make Python development enjoyable. PyCharm supports multiple testing frameworks, including py.test, which is popular in the Python community. Here is how to configure py.test tests in Python:

## Install the pytest Package

The first step to configuring PyCharm for py.test tests in Python is to install the py.test package. You can install the py.test package using pip. Open your terminal and run the following command:

```
pip install pytest
```

This command installs the py.test package on your computer.

## Create a Test File

Now that you have the py.test package installed, the next step is to create a test file. PyCharm supports different types of Python files, including test files. You can create a new test file by clicking on **File** >> **New** >> **Python File**. Name your file something like `test_example.py`, and PyCharm will recognize it as a test file.

## Write Your Tests

Now that you have created your test file, the next step is to write your tests using the py.test syntax. PyCharm will recognize your test functions and display them in the **Run** menu. Here is an example of a py.test test function:

```python
def test_addition():
    assert 2 + 2 == 4
```

In this example, the `test_addition` function tests if 2 + 2 equals 4. If the test fails, the `assert` statement will raise an exception.

## Run Your Tests

The last step is to run your py.test tests in PyCharm. PyCharm recognizes test files and test functions and displays them in the **Run** menu. You can run all your tests by clicking on the file or folder and selecting **Run 'pytest in test_example'**. Alternatively, you can run individual tests by clicking on the test function and selecting **Run 'pytest for test_addition'**.

In summary, configuring PyCharm for py.test tests in Python involves installing the py.test package, creating a test file, writing your tests, and running your tests. With these steps, you can use PyCharm to test your Python projects using py.test.
