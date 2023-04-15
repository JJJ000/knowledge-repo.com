---
title: How can a "datetime" object be converted to seconds in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can convert a datetime object to seconds by using the `timestamp()` method.
---

**Contents**

[TOC]

Section 1: Importing necessary modules
To convert a `datetime` object to seconds in Python, we need to import the `datetime` module. 

```python
from datetime import datetime
```

Section 2: Converting datetime to epoch time
Epoch time is the number of seconds elapsed since January 1, 1970 (known as the Unix epoch). We can convert a `datetime` object to epoch time using the `timestamp()` method.

```python
dt = datetime(2021, 8, 23, 10, 30, 0) # example datetime object
epoch_time = dt.timestamp()
```

Section 3: Converting epoch time to seconds
The `timestamp()` method returns the number of seconds since January 1, 1970, so we don't need to do any additional conversions. We can simply use the `epoch_time` variable as our result.

```python
seconds = epoch_time
```

Section 4: Putting it all together
Here is the code to convert a `datetime` object to seconds:

```python
from datetime import datetime

dt = datetime(2021, 8, 23, 10, 30, 0) # example datetime object
epoch_time = dt.timestamp()
seconds = epoch_time
print(seconds)
```

This code will output `1629736200.0`, which is the number of seconds elapsed since January 1, 1970 until August 23, 2021 at 10:30:00.
