---
title: What is the method in Python to establish the number of days in a specific month?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: We can determine the number of days for a given month using the built-in calendar module in Python.
---

**Contents**

[TOC]

# Introduction
Python provides built-in functions to work with datetime objects which allows us to get information about days, months, and years. In this tutorial, we will learn how to determine the number of days for a given month in python.

# Using the calendar module
Python's built-in `calendar` module provides a method called `monthrange(year, month)` which returns a tuple containing the first weekday of the month and the number of days in the month. 

```python
import calendar

year = 2021
month = 8
days_in_month = calendar.monthrange(year, month)[1]
print("Number of days in the month:", days_in_month)
```

Output:
```
Number of days in the month: 31
```

# Using the datetime module
Python's built-in `datetime` module provides a class called `datetime` which allows us to work with dates and times. We can create a `datetime` object representing the first day of the month, add one month to it, and subtract one day to get the last day of the month.

```python
from datetime import datetime, timedelta

year = 2021
month = 8

first_day_month = datetime(year, month, 1)
last_day_month = (first_day_month + timedelta(days=calendar.monthrange(year, month)[1]-1)).day

print("Number of days in the month:", last_day_month)
```

Output:
```
Number of days in the month: 31
```

# Conclusion
In this tutorial, we learned two ways to determine the number of days for a given month in python. We can either use the `calendar` module to get the number of days directly or use the `datetime` module to create a `datetime` object and calculate the number of days based on the first and last day of the month.
