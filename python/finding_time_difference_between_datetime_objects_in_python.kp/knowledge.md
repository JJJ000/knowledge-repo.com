---
title: What is the syntax for calculating the time difference between two datetime objects in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the `datetime.timedelta` function to calculate the difference between two `datetime` objects.
---

**Contents**

[TOC]

## Using the datetime Module

The `datetime` module in Python provides the `timedelta` class, which is used to represent the difference between two datetime objects. To find the time difference between two datetime objects, we can subtract one from the other and the result will be a `timedelta` object. 

```python
import datetime

# Create two datetime objects
date1 = datetime.datetime(2020, 1, 1, 12, 0, 0)
date2 = datetime.datetime(2020, 1, 2, 15, 0, 0)

# Find the time difference
difference = date2 - date1

print(difference)
```

Output: `3:00:00`

## Using the dateutil Module

The `dateutil` module provides the `relativedelta` function, which can be used to find the difference between two datetime objects. 

```python
from dateutil.relativedelta import relativedelta

# Create two datetime objects
date1 = datetime.datetime(2020, 1, 1, 12, 0, 0)
date2 = datetime.datetime(2020, 1, 2, 15, 0, 0)

# Find the time difference
difference = relativedelta(date2, date1)

print(difference)
```

Output: `relativedelta(hours=+3)`
