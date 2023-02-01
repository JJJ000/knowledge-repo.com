---
title: Calculating a future date in Python using a given number of days
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: To add days to a date in Python, use the timedelta() method from the datetime module.
---

**Contents**

[TOC]

# Using the datetime Module

The `datetime` module in Python provides the `timedelta` object which can be used to add or subtract days from a given date. 

```
from datetime import date, timedelta

today = date.today()

new_date = today + timedelta(days=7)

print(new_date)
```

The above code will add 7 days to the current date and print the new date.

# Using the dateutil Module

The `dateutil` module provides a more flexible way of adding days to a given date. 

```
from dateutil.relativedelta import relativedelta

today = date.today()

new_date = today + relativedelta(days=7)

print(new_date)
```

The above code will add 7 days to the current date and print the new date.

# Using the calendar Module

The `calendar` module provides a way of adding days to a given date by using the `monthrange()` function. 

```
import calendar

today = date.today()

year, month, day = today.year, today.month, today.day

new_date = date(year, month, day + calendar.monthrange(year, month)[1])

print(new_date)
```

The above code will add the number of days in the current month to the current date and print the new date.
