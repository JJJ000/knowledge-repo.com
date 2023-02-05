---
title: What is the process for transforming a time.struct_time object into a datetime object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the datetime.datetime.fromtimestamp() method to convert a time.struct\_time object into a datetime object in Python.
---

**Contents**

[TOC]

# Section 1: Import the Necessary Libraries

To convert a time.struct_time object into a datetime object, the datetime library must be imported. 

```python
import datetime
```

# Section 2: Create a datetime Object from the time.struct_time Object

The `datetime.datetime.fromtimestamp()` method can be used to create a datetime object from a time.struct_time object. 

```python
time_struct = time.struct_time(tm_year=2020, tm_mon=2, tm_mday=2, tm_hour=15, tm_min=30, tm_sec=0, tm_wday=6, tm_yday=33, tm_isdst=-1)

datetime_object = datetime.datetime.fromtimestamp(time.mktime(time_struct))
```

# Section 3: Print the datetime Object

The datetime object can be printed using the `strftime()` method. 

```python
print(datetime_object.strftime("%Y-%m-%d %H:%M:%S"))
```

# Section 4: Output

The output of the code in Section 3 will be:

```
2020-02-02 15:30:00
```
