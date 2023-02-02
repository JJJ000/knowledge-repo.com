---
title: What is the procedure for executing all Python unit tests in a given folder?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Run `python -m unittest discover` in the directory containing the tests.
---

**Contents**

[TOC]

#1: Using unittest

Unittest is a built-in Python module that can be used to run unit tests in a directory. The unittest module provides a command-line interface for running tests.

#2: Setting up the Test Suite

To use the unittest module, you'll need to create a test suite. This is a collection of tests that will be run together. You can create a test suite by creating a file called test_suite.py in your directory. This file should contain the following code:

```
import unittest

def suite():
  test_suite = unittest.TestSuite()
  test_suite.addTest(unittest.makeSuite(TestClassName))
  return test_suite

if __name__ == '__main__':
  unittest.main(defaultTest='suite')
```

Replace TestClassName with the name of the class for which you want to run tests.

#3: Running the Tests

Once the test suite is set up, you can run the tests by running the following command in the terminal:

```
python test_suite.py
```

#4: Output

The unittest module will output the results of the tests. It will display which tests passed and which tests failed.
