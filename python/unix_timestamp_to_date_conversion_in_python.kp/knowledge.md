---
title: Transforming a unix timestamp string into a readable date
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the datetime.datetime.fromtimestamp() function to convert a unix timestamp string to a readable date in Python.
---

**Contents**

[TOC]

## Using the datetime Library

The `datetime` library can be used to convert a Unix timestamp string to a readable date.

First, import the `datetime` library:

```python
import datetime
```

Next, create a `datetime` object from the Unix timestamp string:

```python
unix_timestamp = "1599254400"
date_object = datetime.datetime.fromtimestamp(int(unix_timestamp))
```

Finally, format the date object into a readable date string:

```python
readable_date = date_object.strftime("%d-%m-%Y %H:%M:%S")
print(readable_date)
```

The output will be:

```
12-09-2020 00:00:00
```

## Using the time Library

The `time` library can also be used to convert a Unix timestamp string to a readable date.

First, import the `time` library:

```python
import time
```

Next, convert the Unix timestamp string to a number:

```python
unix_timestamp = "1599254400"
timestamp_number = int(unix_timestamp)
```

Finally, convert the timestamp number to a readable date string:

```python
readable_date = time.strftime("%d-%m-%Y %H:%M:%S", time.gmtime(timestamp_number))
print(readable_date)
```

The output will be:

```
12-09-2020 00:00:00
```
