---
title: Converting a Python string representing a date into a Python date object
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the datetime.strptime() method to convert a string representing a date to a date object.
---

**Contents**

[TOC]

### Converting a Date String to Date Object

Python provides a number of ways to convert a date string to a date object. The most common approach is to use the built-in `datetime` module.

### Using the datetime Module

The `datetime` module provides a number of classes and functions for manipulating dates and times. The `datetime.strptime()` function is used to convert a date string to a date object. It takes two parameters: the date string and the format of the date string.

For example, to convert the date string "2020-02-14" to a date object, you can use the following code:

```
import datetime
date_string = "2020-02-14"
date_object = datetime.strptime(date_string, "%Y-%m-%d")
```

### Using the dateutil Module

The `dateutil` module also provides a number of classes and functions for manipulating dates and times. The `dateutil.parser.parse()` function is used to convert a date string to a date object. It takes one parameter: the date string.

For example, to convert the date string "2020-02-14" to a date object, you can use the following code:

```
from dateutil import parser
date_string = "2020-02-14"
date_object = parser.parse(date_string)
```
