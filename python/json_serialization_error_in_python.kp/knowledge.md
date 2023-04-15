---
title: How can the error message "typeerror (integer) is not JSON serializable" be resolved while attempting to serialize JSON in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The integer values need to be converted to strings before serializing JSON.
---

**Contents**

[TOC]

Section 1: Overview 
When serializing JSON in Python, you may encounter a "TypeError: (Integer) is not JSON serializable" error message. This error occurs when you try to serialize a non-serializable data type, such as an integer, into JSON format.  

Section 2: Causes of the error 
This error can occur for a variety of reasons. One common reason is that you are trying to serialize an object that is not JSON serializable. For example, a Python object that contains non-serializable data types, such as datetime objects or custom classes, may raise this error. Another reason is that you are trying to serialize an integer that is larger than the maximum value that can be represented in JSON.

Section 3: How to fix the error 
To fix this error, you can either serialize the data in a different format or use a JSON encoder that can handle non-serializable data types. If the data is not JSON serializable, you can convert it to a JSON-serializable data type before serialization. For example, you can convert a datetime object to a string using the strftime method. Alternatively, you can use a custom JSON encoder that can handle the non-serializable data type. 

Section 4: Examples of fixing the error 
Here is an example of how to fix the error by converting a datetime object to a string before serialization: 

```
import json 
import datetime 

now = datetime.datetime.now() 
# Attempt to serialize datetime object
try: 
    json.dumps(now) 
except TypeError as e: 
    print("Error:", e) 

# Convert datetime object to string before serializing 
now_str = now.strftime("%Y-%m-%d %H:%M:%S") 
json.dumps(now_str) 
```

Alternatively, you can create a custom JSON encoder that can handle the non-serializable data type. Here is an example of how to create a custom encoder that can handle datetime objects: 

```
import json 
import datetime 

class DateTimeEncoder(json.JSONEncoder): 
    def default(self, obj): 
        if isinstance(obj, datetime.datetime): 
            return obj.strftime("%Y-%m-%d %H:%M:%S") 
        return json.JSONEncoder.default(self, obj) 

now = datetime.datetime.now() 
# Serialize datetime object using custom encoder 
json.dumps(now, cls=DateTimeEncoder)
```

In this example, the default method of the encoder is overridden to handle datetime objects by converting them to a string before serialization.
