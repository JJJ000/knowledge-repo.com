---
title: In python, change the date and time format to unix timestamp and then revert it back
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: To convert datetime to Unix timestamp in python, use the method datetime.timestamp(), and to convert Unix timestamp back to datetime, use the method datetime.fromtimestamp().
---

**Contents**

[TOC]

## Convert datetime to Unix timestamp

We can use the `datetime` module in python to generate datetime objects. Once we have the datetime object, we can convert it into Unix timestamp using the `timestamp()` function. Here is an example:

```python
import datetime

# Generate a datetime object
dt = datetime.datetime.now()

# Convert datetime object to Unix timestamp
timestamp = dt.timestamp()

print(f"Unix timestamp: {timestamp}")
```

In this example, we generate a datetime object using `datetime.datetime.now()` function, and then convert it into Unix timestamp using `timestamp()` function. The resulting Unix timestamp is stored in the `timestamp` variable.

## Convert Unix timestamp to datetime

We can convert Unix timestamp back to datetime object using the `fromtimestamp()` function of datetime module. Here is an example:

```python
import datetime

# UNIX timestamp
timestamp = 1626365478.0

# Convert UNIX timestamp to datetime object
dt = datetime.datetime.fromtimestamp(timestamp)

print(f"Datetime object: {dt}")
```

In this example, we have a Unix timestamp stored in the `timestamp` variable. We convert this Unix timestamp into datetime object using `datetime.datetime.fromtimestamp()` function. The resulting datetime object is stored in the `dt` variable.

## Handling Timezone issues

When converting datetime objects to Unix timestamp, and vice versa, there might be timezone issues. To handle timezone issues, we can use the `pytz` module in python.

Here is an example of converting datetime object to Unix timestamp, while providing timezone information:

```python
import datetime
import pytz

# Create a timezone object
timezone = pytz.timezone('Asia/Kolkata')

# Generate a datetime object
dt = datetime.datetime.now(timezone)

# Convert datetime object to Unix timestamp
timestamp = dt.timestamp()

print(f"Unix timestamp: {timestamp}")
```

In this example, we create a timezone object using `pytz.timezone()` function, and then generate a datetime object using `datetime.datetime.now()` function by passing the timezone object. Finally, we use `timestamp()` function to convert the datetime object to Unix timestamp. The resulting Unix timestamp will be in UTC, but the datetime object is obtained based on the timezone information provided.

Here is an example of converting Unix timestamp to datetime object with timezone:

```python
import datetime
import pytz

# UNIX timestamp
timestamp = 1626365478.0

# Create a timezone object
timezone = pytz.timezone('Asia/Kolkata')

# Convert UNIX timestamp to datetime object
dt = datetime.datetime.fromtimestamp(timestamp, timezone)

print(f"Datetime object with timezone: {dt}")
```

In this example, we create a timezone object using `pytz.timezone()` function, and then convert the Unix timestamp to datetime object using `datetime.datetime.fromtimestamp()` function, by passing both the timestamp and timezone objects. The resulting datetime object will be in the timezone specified.
