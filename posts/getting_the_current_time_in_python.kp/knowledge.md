---
title: How to get the current time?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-08 00:00:00
updated_at: 2023-01-08 00:00:00
tldr: You can use the `datetime.datetime.now()` function to get the current time in Python.
---

**Contents**

[TOC]

### Using the `datetime` Module

The `datetime` module provides various classes to work with dates and times. To get the current time, you can use the `datetime.now()` method.

```python
import datetime

now = datetime.datetime.now()
print(now)
```

### Using the `time` Module

The `time` module provides access to various time-related functions. To get the current time, you can use the `time.time()` function.

```python
import time

now = time.time()
print(now)
```

### Using the `calendar` Module

The `calendar` module provides access to various calendar-related functions. To get the current time, you can use the `calendar.timegm()` function.

```python
import calendar

now = calendar.timegm(time.gmtime())
print(now)
```

### Using the `pytz` Module

The `pytz` module provides access to timezone-related functions. To get the current time, you can use the `pytz.utc.localize()` function.

```python
import pytz
from datetime import datetime

now = pytz.utc.localize(datetime.utcnow())
print(now)
```
