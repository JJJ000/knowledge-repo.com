---
title: What day of the week is associated with a particular date?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: You can use the datetime module`s datetime.date.weekday() method to get the day of week from a given date in Python.
---

**Contents**

[TOC]

## Using the datetime Module 
The `datetime` module provides a `date` class that can be used to get the day of week from a given date.

### Example
```python
from datetime import date

# Create a date object
d = date(2020, 4, 15)

# Get the day of week
print(d.weekday())
```

Output:
```
2
```

## Using the calendar Module
The `calendar` module provides a `weekday` function that can be used to get the day of week from a given date.

### Example
```python
import calendar

# Get the day of week
print(calendar.weekday(2020, 4, 15))
```

Output:
```
2
```
