---
title: How to use strftime to convert a datetime object in Python to epoch format?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: It is not possible to use strftime to convert a Python datetime object to epoch time, as strftime only formats a datetime object into a string.
---

**Contents**

[TOC]

## Step 1: Import datetime module

We need to import the datetime module in order to work with date and time.

```python
import datetime
```


## Step 2: Convert datetime to epoch

To convert datetime to epoch using strftime, we need to follow these steps:

1. Get the datetime object
2. Use strftime to convert the datetime object to a string in the desired format
3. Use strptime to convert the string to a datetime object with the desired format
4. Get the total seconds from the datetime object using the timestamp method

Here's the code to do this:

```python
import datetime

# get the datetime object
my_datetime = datetime.datetime.now()

# convert datetime to epoch using strftime
epoch = int(my_datetime.strftime('%s'))

print(epoch)
```

This will output the number of seconds since the epoch, which is January 1, 1970.


## Step 3: Handling timezone information

If you need to handle timezone information, you can use the pytz module. Here's an example:

```python
import datetime
import pytz

# create a timezone object
tz = pytz.timezone('America/New_York')

# get the datetime object with timezone information
my_datetime = datetime.datetime.now(tz)

# convert datetime to epoch using strftime
epoch = int(my_datetime.strftime('%s'))

print(epoch)
```

Note that the output will still be in UTC. If you need to convert it to local time, you can use the utc_offset method of the timezone object:

```python
# get the UTC offset in seconds for the current timezone
utc_offset = tz.utcoffset(my_datetime).total_seconds()

# adjust the epoch time for the UTC offset
epoch += utc_offset

print(epoch)
```

This will output the epoch time adjusted for the UTC offset.
