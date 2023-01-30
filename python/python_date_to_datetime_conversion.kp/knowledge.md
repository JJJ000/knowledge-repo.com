---
title: Transform a date into a datetime object in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the datetime.strptime() function to convert a date string to a datetime object in Python.
---

**Contents**

[TOC]

### Using the datetime Module

The `datetime` module provides a number of functions and classes to help with date and time manipulation. To convert a date to a datetime object, you can use the `datetime.combine()` method. The `datetime.combine()` method takes two arguments: a `date` object and a `time` object.

```
from datetime import date, time, datetime

# Create a date object
date_obj = date(2020, 5, 20)

# Create a time object
time_obj = time(12, 0, 0)

# Convert date and time to datetime object
datetime_obj = datetime.combine(date_obj, time_obj)
```

### Using the strptime() Method

The `datetime.strptime()` method can also be used to convert a date string to a datetime object. The `strptime()` method takes two arguments: a string representing the date and a string representing the format of the date.

```
from datetime import datetime

# Convert date string to datetime object
datetime_obj = datetime.strptime('20-05-2020 12:00:00', '%d-%m-%Y %H:%M:%S')
```

### Using the strftime() Method

The `datetime.strftime()` method can be used to convert a datetime object to a date string. The `strftime()` method takes one argument: a string representing the format of the date.

```
from datetime import datetime

# Create a datetime object
datetime_obj = datetime(2020, 5, 20, 12, 0, 0)

# Convert datetime object to date string
date_str = datetime_obj.strftime('%d-%m-%Y %H:%M:%S')
```
