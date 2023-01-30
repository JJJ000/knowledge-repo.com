---
title: What steps can I take to resolve the issue of "datetime.datetime not being JSON serializable"?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the json.dumps() method with the default parameter `default=str` to convert the datetime object to a string before serializing.
---

**Contents**

[TOC]

# Section 1: Understand the Problem

The "datetime.datetime not JSON serializable" error occurs when a Python datetime object is attempted to be converted to JSON format. This error is raised because the JSON format does not natively support the datetime object, and therefore it must be converted to a supported format before being serialized.

# Section 2: Use an Alternative Format

One way to overcome this error is to convert the datetime object to a supported format before attempting to serialize it. This can be done by converting the datetime object to a string or an integer format. 

For example, the following code will convert a datetime object to a string in ISO format:

```
import datetime

dt = datetime.datetime.now()

dt_str = dt.isoformat()
```

# Section 3: Use a Serializer

Alternatively, you can use a serializer to convert the datetime object to a supported format. A serializer is a library or module that can be used to convert objects to JSON. 

The Python library jsonpickle is a popular choice for serializing objects to JSON. The following code will serialize a datetime object to JSON using jsonpickle:

```
import datetime
import jsonpickle

dt = datetime.datetime.now()

dt_json = jsonpickle.encode(dt)
```

# Section 4: Use a Custom Encoder

Finally, you can create a custom encoder to convert the datetime object to JSON. A custom encoder is a class that implements the JSONEncoder class and overrides the default encoder to support custom objects.

The following code will create a custom encoder to convert a datetime object to JSON:

```
import datetime
import json

class DateTimeEncoder(json.JSONEncoder):
    def default(self, o):
        if isinstance(o, datetime.datetime):
            return o.isoformat()

        return json.JSONEncoder.default(self, o)

dt = datetime.datetime.now()

dt_json = json.dumps(dt, cls=DateTimeEncoder)
```
