---
title: Enable the integration of python's new dataclasses with the Python JSON encoder
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The Python JSON encoder supports Python`s new dataclasses by default.
---

**Contents**

[TOC]

## Introduction

JSON is a widely used format for data exchange between different systems. The `json` module in Python provides a way to encode Python objects in JSON format.

Python 3.7 introduced a new feature called "dataclasses." It provides a way to define classes that are primarily used to store data. In this article, we will discuss how to make the Python JSON encoder support Python's new dataclasses.

## Steps to Make the Python JSON Encoder Support Dataclasses

1. Inherit from the `json.JSONEncoder` class.
2. Override the `default` method of the `JSONEncoder` class.
3. Use the `dataclasses.asdict()` function to convert dataclasses to a dictionary.
4. Use the `json.dumps()` function with the `cls` parameter set to the custom encoder class.

### Step 1: Inherit from the `json.JSONEncoder` class

The first step is to create a custom JSON encoder class that inherits from the `json.JSONEncoder` class. This class will be responsible for encoding dataclasses.

```python
import json

class DataclassEncoder(json.JSONEncoder):
    def default(self, obj):
        pass
```

### Step 2: Override the `default` method of the `JSONEncoder` class

The `default` method is the main method that needs to be overridden in the `DataclassEncoder` class. This method will be called for objects that cannot be encoded by the encoder. In this method, we can check if the object is a dataclass and convert it to a dictionary using the `dataclasses.asdict()` function.

```python
import dataclasses

class DataclassEncoder(json.JSONEncoder):
    def default(self, obj):
        if dataclasses.is_dataclass(obj):
            return dataclasses.asdict(obj)
        return super().default(obj)
```

### Step 3: Use the `dataclasses.asdict()` function to convert dataclasses to a dictionary

The `dataclasses.asdict()` function can be used to convert dataclasses to a dictionary. It takes a dataclass object as input and returns a dictionary.

### Step 4: Use the `json.dumps()` function with the `cls` parameter set to the custom encoder class

Once the `DataclassEncoder` class is defined, it can be used with the `json.dumps()` function to encode dataclasses in JSON format. The `cls` parameter of the `json.dumps()` function should be set to the `DataclassEncoder` class.

```python
import json
import dataclasses

class DataclassEncoder(json.JSONEncoder):
    def default(self, obj):
        if dataclasses.is_dataclass(obj):
            return dataclasses.asdict(obj)
        return super().default(obj)

@dataclasses.dataclass
class Person:
    name: str
    age: int

person = Person(name='Alice', age=30)
json_data = json.dumps(person, cls=DataclassEncoder)
print(json_data)
```

This code will output the following JSON string:

```json
{"name": "Alice", "age": 30}
```

## Conclusion

In this article, we have discussed how to make the Python JSON encoder support Python's new dataclasses. We have created a custom JSON encoder class that can encode dataclasses. We have used the `dataclasses.asdict()` function to convert dataclasses to a dictionary and the `json.dumps()` function to encode the dictionary in JSON format.
