---
title: What is the process of changing a datetime to a date?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the datetime.date() method to convert a datetime object to a date object.
---

**Contents**

[TOC]

### Using the datetime module

The `datetime` module provides classes for manipulating dates and times in both simple and complex ways. To convert a `datetime` object to a `date` object, use the `date()` method.

```python
from datetime import datetime

# Create a datetime object
date_time = datetime(2020, 8, 2, 12, 30, 45)

# Convert to a date object
date = date_time.date()

print(date)  # Output: 2020-08-02
```

### Using the dateutil module

The `dateutil` module provides powerful extensions to the standard datetime module, including the ability to convert a `datetime` object to a `date` object. To do this, use the `datetime.date()` method.

```python
from dateutil import parser

# Create a datetime object
date_time = parser.parse("2020-08-02 12:30:45")

# Convert to a date object
date = date_time.date()

print(date)  # Output: 2020-08-02
```

### Using the time module

The `time` module provides a number of functions for manipulating dates and times. To convert a `datetime` object to a `date` object, use the `time.strptime()` method.

```python
import time

# Create a datetime object
date_time = time.strptime("2020-08-02 12:30:45", "%Y-%m-%d %H:%M:%S")

# Convert to a date object
date = date_time.date()

print(date)  # Output: 2020-08-02
```

### Using the calendar module

The `calendar` module provides functions for working with dates in a variety of ways. To convert a `datetime` object to a `date` object, use the `calendar.timegm()` method.

```python
import calendar

# Create a datetime object
date_time = calendar.timegm("2020-08-02 12:30:45")

# Convert to a date object
date = date_time.date()

print(date)  # Output: 2020-08-02
```
