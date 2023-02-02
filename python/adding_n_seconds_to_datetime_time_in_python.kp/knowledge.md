---
title: How can I add n seconds to a datetime.time object in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: The standard way to add N seconds to datetime.time in Python is to use the timedelta() method.
---

**Contents**

[TOC]

### Using timedelta
The standard way to add N seconds to datetime.time in Python is to use the timedelta class. 

### Syntax
The syntax for using timedelta is as follows:

```
from datetime import timedelta

my_time = datetime.time(hour=12, minute=30, second=15)

new_time = my_time + timedelta(seconds=N)
```

### Example
For example, if you want to add 30 seconds to the time 12:30:15, you would use the following code:

```
from datetime import timedelta

my_time = datetime.time(hour=12, minute=30, second=15)

new_time = my_time + timedelta(seconds=30)

print(new_time) # 12:30:45
```

### Output
The output of the code above would be 12:30:45.
