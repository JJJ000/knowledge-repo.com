---
title: Setup and teardown methods for multiple unit tests
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: setUp and tearDown methods are useful for setting up and cleaning up test fixtures that are required by several unit tests in Python.
---

**Contents**

[TOC]

Creating a setUp() function in Python

```python
def setUp(self):
    # code to set up resources
```

The setUp() function is executed before each individual test case in a unittest.TestCase class. In this function, resources required by the test cases can be set up, such as creating temporary files or initializing database connections.

Creating a tearDown() function in Python

```python
def tearDown(self):
    # code to tear down resources
```

The tearDown() function is executed after each individual test case in a unittest.TestCase class. In this function, resources created in the setUp() function can be cleaned up or destroyed, such as deleting temporary files or closing database connections.

Using setUp() and tearDown() in multiple test cases

```python
import unittest

class TestMath(unittest.TestCase):

    def setUp(self):
        # set up resources for all tests
        self.x = 5
        self.y = 10

    def tearDown(self):
        # clean up resources created in setUp()
        pass

    def test_add(self):
        result = self.x + self.y
        self.assertEqual(result, 15)

    def test_subtract(self):
        result = self.y - self.x
        self.assertEqual(result, 5)

if __name__ == '__main__':
    unittest.main()
```

The setUp() and tearDown() functions can be used across multiple test cases in the same unittest.TestCase class. In this example, both the test_add() and test_subtract() functions use the resources set up in the setUp() function, and the tearDown() function is called after each test case is executed to clean up any resources created by the setUp() function. 

Using setUpClass() and tearDownClass() for class-level setup and teardown

```python
import unittest

class TestMath(unittest.TestCase):

    @classmethod
    def setUpClass(cls):
        # set up resources for all tests in the class
        pass

    @classmethod
    def tearDownClass(cls):
        # clean up resources created in setUpClass()
        pass

    def setUp(self):
        # set up resources for each test case
        self.x = 5
        self.y = 10

    def tearDown(self):
        # clean up resources created in setUp()
        pass

    def test_add(self):
        result = self.x + self.y
        self.assertEqual(result, 15)

    def test_subtract(self):
        result = self.y - self.x
        self.assertEqual(result, 5)

if __name__ == '__main__':
    unittest.main()
```

The setUpClass() and tearDownClass() functions are executed once per test class, rather than once per test case like setUp() and tearDown(). This can be used to set up resources that are shared by all test cases in a class, such as establishing a database connection or loading a large file. In this example, the setUpClass() and tearDownClass() functions are defined, but do not do anything.
