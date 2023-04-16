---
title: What is the process for changing a local time string to utc?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the pytz library to convert a local time string to UTC in Python.
---

**Contents**

[TOC]

#Section 1: Import Libraries

In order to convert local time strings to UTC, we will need to import the `pytz` and `datetime` libraries.

```python
import pytz
from datetime import datetime
```

#Section 2: Retrieve Local Time

We will need to retrieve the local time from the string. We can use the `datetime.strptime` function to parse the local time string into a `datetime` object.

```python
local_time = datetime.strptime('Tue Mar 10 13:00:00 2020', '%a %b %d %H:%M:%S %Y')
```

#Section 3: Set Timezone

We can use the `pytz` library to set the timezone of the `datetime` object.

```python
local_tz = pytz.timezone('US/Pacific')
local_time = local_tz.localize(local_time)
```

#Section 4: Convert to UTC

Finally, we can use the `astimezone` function to convert the local time to UTC.

```python
utc_time = local_time.astimezone(pytz.utc)
```
