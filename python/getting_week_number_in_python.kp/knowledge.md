---
title: What is the syntax for finding the week number in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The week number can be obtained using the datetime.date.isocalendar() method.
---

**Contents**

[TOC]

# Using datetime module
The datetime module provides a number of different classes and functions to manipulate dates and times. To get the week number using the datetime module, use the isocalendar() method.

```
import datetime

date = datetime.date(2019, 5, 1)
week_number = date.isocalendar()[1]
print(week_number)
```

# Using calendar module
The calendar module provides a number of useful functions for working with dates and times. To get the week number using the calendar module, use the calendar.weekday() method.

```
import calendar

date = (2019, 5, 1)
week_number = calendar.weekday(*date)
print(week_number)
```

# Using strftime()
The strftime() method can be used to get the week number from a date.

```
import datetime

date = datetime.date(2019, 5, 1)
week_number = date.strftime("%W")
print(week_number)
```

# Using timedelta
The timedelta class can be used to calculate the difference between two dates. To get the week number using timedelta, subtract the two dates and divide the result by seven.

```
from datetime import date, timedelta

start_date = date(2019, 5, 1)
end_date = date(2019, 5, 8)

diff = end_date - start_date
week_number = diff.days // 7
print(week_number)
```
