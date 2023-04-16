---
title: What is the simplest method for obtaining the current gmt time in unix timestamp format?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The easiest way to get current GMT time in Unix timestamp format in Python is to use the time.time() function.
---

**Contents**

[TOC]

### Using Time Module
The easiest way to get current GMT time in Unix timestamp format in Python is by using the [time module](https://docs.python.org/3/library/time.html). To do this, you can use the `time.time()` method, which will return the current time in Unix timestamp format.

```python
import time

current_time = time.time()
print(current_time)
```

### Using Datetime Module
Another way to get current GMT time in Unix timestamp format in Python is by using the [datetime module](https://docs.python.org/3/library/datetime.html). To do this, you can use the `datetime.utcnow()` method, which will return the current UTC time in datetime object format. Then, you can use the `timestamp()` method to convert the datetime object to Unix timestamp format.

```python
from datetime import datetime

current_time = datetime.utcnow()
unix_timestamp = current_time.timestamp()
print(unix_timestamp)
```
