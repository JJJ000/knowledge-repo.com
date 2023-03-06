---
title: Converting an instance of a class to JSON format
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: You can use the built-in JSON module in Python to serialize a class instance to JSON by defining a custom JSON encoder for the class.
---

**Contents**

[TOC]

## Introduction

Serialization is the process of converting a specific data structure, such as an object or a dictionary, into a more common format, such as JSON or XML. This is useful when transmitting data over a network, storing data in a file, or passing data between different programming languages.

In this tutorial, we'll focus on serializing a Python class instance to JSON format.


## Serializing a Class Instance to JSON

To serialize a class instance to JSON, we first need to convert it to a dictionary. We can do this by implementing a method in our class that returns a dictionary representation of the instance's properties. We'll call this method `to_dict()`.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def to_dict(self):
        return {
            'name': self.name,
            'age': self.age
        }
```

Next, we can use the `json.dumps()` function to convert the dictionary to JSON format:

```python
import json

person = Person('John Smith', 30)
person_json = json.dumps(person.to_dict())
print(person_json)
```

This will output the following JSON string:

```
{"name": "John Smith", "age": 30}
```


## Handling Complex Objects

The approach outlined above works well for simple classes with basic properties. However, if the class has more complex properties, such as other objects or lists, we need to take additional steps.

First, we need to ensure that any non-serializable properties are converted to serializable equivalents. For example, if our class contained a `datetime` object, we would need to convert it to a string representation.

We can do this by providing a custom function to the `json.dumps()` function's `default` parameter. This function will be called for any non-serializable objects, and should return a serializable representation of the object.

```python
import json
import datetime

class Person:
    def __init__(self, name, age, birthdate):
        self.name = name
        self.age = age
        self.birthdate = birthdate

    def to_dict(self):
        return {
            'name': self.name,
            'age': self.age,
            'birthdate': self.birthdate
        }

def serialize_date(obj):
    if isinstance(obj, datetime.date):
        return obj.isoformat()

person = Person('John Smith', 30, datetime.date(1990, 1, 1))
person_json = json.dumps(person.to_dict(), default=serialize_date)
print(person_json)
```

This will output the following JSON string, with the birthdate property serialized as a string:

```
{"name": "John Smith", "age": 30, "birthdate": "1990-01-01"}
```


## Conclusion

Serializing a class instance to JSON in Python is relatively straightforward. We need to convert the instance to a dictionary, and then use the `json.dumps()` function to convert it to the desired format. If the class has complex properties, we need to provide custom serialization functions to handle them appropriately.
