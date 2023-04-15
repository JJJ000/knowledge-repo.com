---
title: I attempted to ridicule datetime.date.today(), but it was unsuccessful
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: Mocking datetime.date.today() alone won`t work because it`s a class method - you need to mock the entire datetime.date class instead.
---

**Contents**

[TOC]

Section 1: Introduction
In Python, the datetime module provides classes for working with dates and times. One such class is datetime.date which represents a calendar date (year, month, day). Often in testing, we need to mock the current date for our tests. The most common method to get the current date is datetime.date.today(). We may want to mock this function to test our program's behavior with different dates.

Section 2: Attempted solution
To mock datetime.date.today() method in Python, we can use the unittest.mock module. We can import the MagicMock class from this module, which allows us to create a mock object.

Here is how it can be done in Python:

```
import datetime
from unittest.mock import MagicMock

# Mock datetime.date.today() method
datetime.date.today = MagicMock(return_value=datetime.date(2021, 8, 24))

# Test your code
```

Section 3: Explanation
In the above code, we are first importing datetime module and MagicMock class from the unittest.mock module.

Next, we are mocking the datetime.date.today() method by assigning it to MagicMock. We are also specifying the return value of this method to be a date object representing the date 2021-08-24.

Now when we call datetime.date.today() method in any part of our code, it will return the date 2021-08-24 instead of the actual current date. This allows us to test our program's behavior with a fixed date.

Section 4: Possible issues
While mocking datetime.date.today() method, we need to ensure that it is properly imported in all parts of our code. If it is imported as a relative import, it may not be able to be mocked properly.

Also, we need to be cautious in our testing that we don't have any hardcoded dates in our code that could lead to inconsistency in our test cases.
