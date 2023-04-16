---
title: What is the syntax for retrieving the current date and time in Python and dividing it into its components of year, month, day, hour, and minute?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the datetime.now() function to get the current time in Python and then use the strftime() method to break it up into year, month, day, hour, and minute.
---

**Contents**

[TOC]

### Using datetime

The `datetime` module provides classes for manipulating dates and times in both simple and complex ways.

```python
import datetime

now = datetime.datetime.now()

year = now.year
month = now.month
day = now.day
hour = now.hour
minute = now.minute
```

### Using time

The `time` module provides various time-related functions.

```python
import time

t = time.localtime()

year = t.tm_year
month = t.tm_mon
day = t.tm_mday
hour = t.tm_hour
minute = t.tm_min
```
