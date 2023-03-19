---
title: What is the method to eliminate a pytz timezone from a datetime object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: You can remove a pytz timezone from a datetime object by using the replace method and passing in None as the timezone argument.
---

**Contents**

[TOC]

## Getting the datetime object

The first step is to obtain the datetime object that we want to remove the timezone from. This can be done in a number of ways, depending on how the datetime is being generated or obtained. For example, we could use the `datetime.now()` function to get the current datetime, or we could parse a datetime string using the `datetime.strptime()` function.

```python
import datetime

# Get the current datetime
dt = datetime.datetime.now()

# Parse a datetime string
dt_string = '2022-01-01 12:00:00'
dt = datetime.datetime.strptime(dt_string, '%Y-%m-%d %H:%M:%S')
```

## Removing the timezone information

Once we have the datetime object, we can remove the timezone information by converting it to a naive datetime object. A naive datetime object is one that does not have any timezone information associated with it.

We can convert a datetime object to a naive datetime object by using the `datetime.replace()` method and setting the `tzinfo` parameter to `None`.

```python
naive_dt = dt.replace(tzinfo=None)
```

## Testing the result

We can test the result to make sure that the timezone information has been removed from the datetime object. We can do this by printing out the values of the `datetime.tzinfo` attribute for both the original datetime object and the naive datetime object.

```python
print(dt.tzinfo)         # prints None or the timezone object that was set
print(naive_dt.tzinfo)   # prints None
```

If the timezone information has been successfully removed, the `dt.tzinfo` value should be `None` or the timezone object that was set, while the `naive_dt.tzinfo` value should be `None`.

## Final code

Putting it all together, our code for removing the timezone information from a datetime object would look like this:

```python
import datetime

# Get the datetime object
dt = datetime.datetime.now()

# Remove the timezone information
naive_dt = dt.replace(tzinfo=None)

# Test the result
print(dt.tzinfo)         # prints None or the timezone object that was set
print(naive_dt.tzinfo)   # prints None
```
