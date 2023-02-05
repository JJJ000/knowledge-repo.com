---
title: What is the most efficient way to use the standard library to convert a utc datetime to a local datetime?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the datetime.astimezone() method to convert a UTC datetime to a local datetime.
---

**Contents**

[TOC]

# Section 1: Import Libraries

The following libraries will be needed to convert a UTC datetime to a local datetime:

```python
import datetime
import pytz
```

# Section 2: Create UTC Datetime

The following code will create a UTC datetime object:

```python
utc_datetime = datetime.datetime.utcnow()
```

# Section 3: Convert to Local Datetime

The following code will convert the UTC datetime to a local datetime object:

```python
local_tz = pytz.timezone('America/New_York')
local_datetime = utc_datetime.astimezone(local_tz)
```

# Section 4: Print Local Datetime

The following code will print the local datetime object:

```python
print(local_datetime)
```
