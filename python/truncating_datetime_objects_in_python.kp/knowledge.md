---
title: What is the process for reducing the time part of a datetime object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the datetime.date() method to truncate the time from a datetime object.
---

**Contents**

[TOC]

### Using strftime()
The `strftime()` method of datetime objects allows you to format a datetime object to a given format. To truncate the time on a datetime object, you can use the `%Y-%m-%d` format. This will return a string representation of the datetime object with the time truncated. 

### Example

```
from datetime import datetime

# Create a datetime object
dt = datetime(2020, 8, 1, 10, 15, 20)

# Truncate the time from the datetime object
dt_truncated = dt.strftime('%Y-%m-%d')

# Print the truncated datetime
print(dt_truncated)

# Output: 2020-08-01
```

### Using replace()
The `replace()` method of datetime objects allows you to replace any of the attributes of the datetime object with a given value. To truncate the time on a datetime object, you can use the `replace()` method to set the hours, minutes, seconds, and microseconds to 0. 

### Example

```
from datetime import datetime

# Create a datetime object
dt = datetime(2020, 8, 1, 10, 15, 20)

# Truncate the time from the datetime object
dt_truncated = dt.replace(hour=0, minute=0, second=0, microsecond=0)

# Print the truncated datetime
print(dt_truncated)

# Output: 2020-08-01 00:00:00
```
