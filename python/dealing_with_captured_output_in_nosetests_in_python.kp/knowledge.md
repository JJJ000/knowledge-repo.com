---
title: How can I avoid nosetests from capturing the output produced by my print statements?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the -s or --nocapture command line option when running nosetests to allow print statements to be displayed.
---

**Contents**

[TOC]

Section 1: Background

Python's nose testing library, also called nosetests, is a popular testing tool that allows testing multiple test files with one command. One of the ways nosetests works is by capturing standard output (stdout) and standard error (stderr) for the test functions it runs. This is useful for debugging, but can also be a problem if you have print statements in your test functions that you do not want to be captured.

Section 2: Solution 1 - Redirect stdout

One way to circumvent nosetests capturing print statements is to redirect stdout to a file or a StringIO object in the setUp() function of your test. This involves:

1. Importing the StringIO or sys library
2. Creating a new StringIO object or opening a file in write mode
3. Redirecting stdout to the StringIO object or file using the sys library
4. In the tearDown() function, redirect back to the original stdout.

Here's an example implementation:

```
import sys
from StringIO import StringIO

class TestClass(unittest.TestCase):

    def setUp(self):
        self.stdout = sys.stdout
        sys.stdout = StringIO()

    def tearDown(self):
        sys.stdout = self.stdout

    def test_function(self):
        # your print statements
        print("Hello, world!")

        # test code
        self.assertEqual(some_value, expected_result)

```

Section 3: Solution 2 - Use logging instead of print

Another way to avoid nosetests capturing print statements is to use the logging library instead of print. This involves:

1. Importing the logging library
2. Setting the logging level to a value that will capture the messages you want to see (e.g. logging.DEBUG)
3. Using logging.info(), logging.debug(), or other logging functions instead of print statements.

Here's an example implementation:

```
import logging

class TestClass(unittest.TestCase):

    def test_function(self):
        # configure logging
        logging.basicConfig(level=logging.DEBUG)

        # your logging statements
        logging.info("Hello, world!")

        # test code
        self.assertEqual(some_value, expected_result)
```

Section 4: Conclusion

In summary, two ways to circumvent nosetests capturing print statements are:

1. Redirect stdout to a file or StringIO object in the setUp() function of your test
2. Use the logging library instead of print statements.

Both solutions have their advantages and disadvantages, and the best solution for you will depend on your use case.
