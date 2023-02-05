---
title: Executing a single unit test from unittest.testcase via the command line
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Run the test with the command `python -m unittest <TestCase>.<test\_method>`.
---

**Contents**

[TOC]

1. Install the unittest Module

Before running a single test from unittest.TestCase, the unittest module must be installed. To do this, open the command line and type:

```
pip install unittest
```

2. Create a Test Case

A test case is a collection of tests that can be run together. To create a test case, create a Python file with the following code:

```
import unittest

class MyTestCase(unittest.TestCase):
    def test_something(self):
        self.assertEqual(True, False)

if __name__ == '__main__':
    unittest.main()
```

3. Run the Test Case

To run the test case, open the command line and type:

```
python my_test_case.py
```

4. Run a Single Test

To run a single test from the test case, open the command line and type:

```
python my_test_case.py -v MyTestCase.test_something
```
