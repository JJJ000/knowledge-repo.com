---
title: Retrieve the date corresponding to a given week number
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `datetime` module in Python to convert week number to date, as shown `datetime.datetime.strptime(f`{week}-{year}-1`, `%W-%Y-%w`).date()`
---

**Contents**

[TOC]

## Problem Statement
Given a week number, our task is to find out the date for the first day of that week in Python.


## Approach
To solve this problem, we can follow the below two approaches:
1. Using the `datetime` module: Python's `datetime` module provides `strptime` method which can be used to parse a string representing a date and time into a `datetime` object. We can use this method to parse the date and then use the `isocalendar` method to get the year, week number, and day of the week for the given date. Finally, we can use these values to calculate the date for the first day of the given week.
2. Using the `dateutil` module: Python's `dateutil` module provides various date and time parsing utilities. We can use the `parse` method of this module to parse the date string and then use the `date` method to get the date object for the given date. Finally, we can use the `relativedelta` method to get the date for the first day of the given week.


### Approach 1: Using the `datetime` module

#### Steps
1. Parse the given date using the `strptime` method of the `datetime` module.
2. Use the `isocalendar` method to get the year, week number, and day of the week for the given date.
3. Calculate the date for the first day of the given week using the formula: `date = given_date - timedelta(days=(day_of_week-1))`.

#### Code
```python
from datetime import datetime, timedelta

def date_from_week_num(week_num, year):
    first_day_of_week = datetime.strptime(f'{year}-W{week_num}-1', "%Y-W%W-%w")
    date = first_day_of_week - timedelta(days=(first_day_of_week.isocalendar()[2]-1))
    return date.strftime("%Y-%m-%d")
```

#### Explanation
- First, we pass the year and week number to the `datetime.strptime()` method which returns the date for the first day of the given week.
- Then, we use the `isocalendar` method to get the year, week number, and day of the week for the given date.
- Finally, we calculate the date for the first day of the given week using the formula `date = given_date - timedelta(days=(day_of_week-1))`, where `day_of_week` is the day of the week for the given date.


### Approach 2: Using the `dateutil` module

#### Steps
1. Parse the given date using the `parse` method of the `dateutil` module.
2. Use the `date` method to get the date object for the given date.
3. Use the `relativedelta` method to get the first day of the week for the given date using the formula: `date = given_date + relativedelta(weekday=MO(-1))`.

#### Code
```python
from dateutil.parser import parse
from dateutil.relativedelta import relativedelta, MO

def date_from_week_num(week_num, year):
    given_date = parse(f'{year}-W{week_num}-1', yearfirst=True)
    first_day_of_week = given_date + relativedelta(weekday=MO(-1))
    return first_day_of_week.strftime("%Y-%m-%d")
```

#### Explanation
- First, we parse the given date using the `parse` method of the `dateutil` module.
- Then, we use the `date` method to get the date object for the given date.
- Finally, we use the `relativedelta` method to get the first day of the week for the given date using the formula `date = given_date + relativedelta(weekday=MO(-1))`, where `MO` stands for "Monday" and `-1` specifies that we want to get the first Monday of the week.
