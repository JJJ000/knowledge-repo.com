---
title: Convert a datetime object into a string with millisecond precision
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the strftime() method with the format string `%Y-%m-%d %H%M%S.%f` to format a datetime into a string with milliseconds.
---

**Contents**

[TOC]

### Using strftime()

The `strftime()` method can be used to format a datetime object into a string with milliseconds. 

```python
import datetime

dt = datetime.datetime(2020, 8, 7, 12, 30, 45, 123456)

dt.strftime('%Y-%m-%d %H:%M:%S.%f')
# '2020-08-07 12:30:45.123456'
```

### Using str.format()

The `str.format()` method can also be used to format a datetime object into a string with milliseconds.

```python
import datetime

dt = datetime.datetime(2020, 8, 7, 12, 30, 45, 123456)

'{:%Y-%m-%d %H:%M:%S.%f}'.format(dt)
# '2020-08-07 12:30:45.123456'
```

### Using time.strftime()

The `time.strftime()` function can also be used to format a datetime object into a string with milliseconds.

```python
import datetime
import time

dt = datetime.datetime(2020, 8, 7, 12, 30, 45, 123456)

time.strftime('%Y-%m-%d %H:%M:%S.%f', dt.timetuple())
# '2020-08-07 12:30:45.123456'
```
