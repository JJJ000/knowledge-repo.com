---
title: What is the best way to resolve the issue of `datetime.datetime` not being json serializable?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-01-16 00:00:00
updated_at: 2023-01-16 00:00:00
tldr: Use a library such as `dateutil` to convert datetime objects to strings that can be serialized to JSON.
---

**Contents**

[TOC]

### Serialize datetime Objects

One way to overcome the "datetime.datetime not JSON serializable" error is to serialize the datetime objects before encoding them into JSON. This can be done using the `json.dumps()` method, which takes an optional argument `default` that can be used to specify a custom serialization function for non-serializable objects. The custom serialization function must accept a single argument, the object to be serialized, and should return a serializable object.

For example, if we want to serialize a datetime object, we can define a custom serialization function like this:

```python
def serialize_datetime(obj):
    if isinstance(obj, datetime.datetime):
        return obj.isoformat()
    else:
        raise TypeError("Type %s not serializable" % type(obj))
```

### Use a Third-Party Library

Another way to overcome the "datetime.datetime not JSON serializable" error is to use a third-party library such as [dateutil](https://dateutil.readthedocs.io/en/stable/). This library provides a `dateutil.parser.parse()` method that can be used to convert a datetime object to a serializable format.

For example, if we have a datetime object `d`, we can serialize it using `dateutil` like this:

```python
import dateutil.parser

serialized_d = dateutil.parser.parse(d)
```

### Convert to String

A third way to overcome the "datetime.datetime not JSON serializable" error is to convert the datetime object to a string before encoding it into JSON. This can be done using the `strftime()` method, which takes a format string as an argument and returns a string representation of the datetime object.

For example, if we have a datetime object `d`, we can convert it to a string like this:

```python
serialized_d = d.strftime("%Y-%m-%d %H:%M:%S")
```

### Convert to Unix Timestamp

A fourth way to overcome the "datetime.datetime not JSON serializable" error is to convert the datetime object to a Unix timestamp before encoding it into JSON. This can be done using the `timestamp()` method, which returns the Unix timestamp of the datetime object.

For example, if we have a datetime object `d`, we can convert it to a Unix timestamp like this:

```python
serialized_d = d.timestamp()
```
