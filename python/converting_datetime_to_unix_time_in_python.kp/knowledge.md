---
title: What is the syntax to convert a datetime object to milliseconds since epoch (unix time) in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the `timestamp()` method of the datetime object to convert it to milliseconds since epoch.
---

**Contents**

[TOC]

# Section 1: Using the Time Module

The `time` module provides a function, `time()`, which returns the current system time in seconds since the epoch. To convert a datetime object to milliseconds, you can use the `datetime.timestamp()` method to return the timestamp in seconds and then multiply it by 1000 to get the milliseconds.

```python
import time
from datetime import datetime

# datetime object
dt = datetime(2020, 4, 17, 12, 0, 0)

# timestamp in seconds
timestamp = dt.timestamp()

# convert to milliseconds
milliseconds = timestamp * 1000

# print result
print(milliseconds)
```

# Section 2: Using the Calendar Module

The `calendar` module provides the `timegm()` function which can be used to convert a `datetime` object to milliseconds since the epoch.

```python
import calendar
from datetime import datetime

# datetime object
dt = datetime(2020, 4, 17, 12, 0, 0)

# convert to milliseconds
milliseconds = calendar.timegm(dt.timetuple()) * 1000

# print result
print(milliseconds)
```

# Section 3: Using the Arrow Module

The `arrow` module provides a `Arrow` class which can be used to convert a `datetime` object to milliseconds since the epoch.

```python
import arrow
from datetime import datetime

# datetime object
dt = datetime(2020, 4, 17, 12, 0, 0)

# convert to milliseconds
milliseconds = arrow.get(dt).timestamp * 1000

# print result
print(milliseconds)
```

# Section 4: Using the Dateutil Module

The `dateutil` module provides the `dateutil.tz.tzutc()` function which can be used to convert a `datetime` object to milliseconds since the epoch.

```python
import dateutil.tz
from datetime import datetime

# datetime object
dt = datetime(2020, 4, 17, 12, 0, 0)

# convert to milliseconds
milliseconds = dt.replace(tzinfo=dateutil.tz.tzutc()).timestamp() * 1000

# print result
print(milliseconds)
```
