---
title: What is the date of the last day of the month?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-30 00:00:00
updated_at: 2023-04-30 00:00:00
tldr: The last day of the month can be obtained using the datetime.date.monthrange() function.
---

**Contents**

[TOC]

# Section 1: Using the datetime Library

The easiest way to get the last day of the month in Python is by using the `datetime` library. This library provides a `date` class that allows you to easily manipulate dates.

# Section 2: Creating a Date Object

First, you'll need to create a `date` object with the current date. This can be done using the `date.today()` method.

```python
from datetime import date

today = date.today()
```

# Section 3: Calculating the Last Day of the Month

Once you have a `date` object, you can calculate the last day of the month by adding one month and subtracting one day.

```python
from datetime import timedelta

last_day = today + timedelta(days=31) - timedelta(days=1)
```

# Section 4: Outputting the Last Day of the Month

Finally, you can output the last day of the month in a variety of formats. For example, you can output it as a string using the `strftime()` method.

```python
last_day_str = last_day.strftime("%B %d, %Y")
print(last_day_str)
```

This will output the last day of the month in the format "Month Day, Year".
