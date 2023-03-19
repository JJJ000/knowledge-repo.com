---
title: What is the method to retrieve utc time in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the datetime module and call datetime.utcnow() method to get current UTC time in Python.
---

**Contents**

[TOC]

## Using datetime module

The datetime module in Python provides classes to work with dates and times. It includes a class called `datetime` which can be used to represent date and time. The `datetime` class provides a method `utcnow()` which returns the current UTC date and time.

```python
from datetime import datetime

utc_time = datetime.utcnow()
print(utc_time)
```

Output:
```
2021-09-23 10:20:30.123456
```

## Using time module

The `time` module in Python provides functions to work with time. It provides a function `gmtime()` which returns the current time in UTC. We can use the `strftime()` function to format the time in any desired format.

```python
import time

utc_time = time.gmtime()
print(time.strftime("%Y-%m-%d %H:%M:%S", utc_time))
```

Output:
```
2021-09-23 10:20:30
```

## Using pytz module

The `pytz` module in Python provides support for working with timezones. We can use the `pytz.utc` timezone to get the current UTC time.

```python
import datetime
import pytz

utc_time = datetime.datetime.now(pytz.utc)
print(utc_time)
```

Output:
```
2021-09-23 10:20:30.123456+00:00
```

## Using arrow module

The `arrow` module in Python provides a simpler and more human-readable way to work with dates and times. We can use the `utcnow()` method of the `arrow` module to get the current UTC time.

```python
import arrow

utc_time = arrow.utcnow()
print(utc_time)
```

Output:
```
2021-09-23T10:20:30.123456+00:00
```
