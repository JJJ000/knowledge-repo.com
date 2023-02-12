---
title: Transform a Python object with changing values into a JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the json.dumps() function to convert a dynamic Python object to JSON.
---

**Contents**

[TOC]

## Using the json Module

Python's built-in `json` module is the easiest way to convert a Python object into a JSON string. To use the `json` module, simply call `json.dumps()` on the object you want to convert.

```python
import json

my_object = {
    'name': 'John Doe',
    'age': 42
}

json_string = json.dumps(my_object)

print(json_string)
# '{"name": "John Doe", "age": 42}'
```

## Using the Pickle Module

The `pickle` module is another way to convert a Python object into a JSON string. The `pickle` module is useful if the object you are trying to convert contains complex data structures. To use the `pickle` module, simply call `pickle.dumps()` on the object you want to convert.

```python
import pickle

my_object = {
    'name': 'John Doe',
    'age': 42
}

json_string = pickle.dumps(my_object)

print(json_string)
# b'\x80\x03}q\x00(X\x04\x00\x00\x00nameq\x01X\x08\x00\x00\x00John Doeq\x02X\x03\x00\x00\x00ageq\x03K*u.'
```

## Using the Simplejson Module

The `simplejson` module is a third way to convert a Python object into a JSON string. The `simplejson` module is useful if you need to customize the way the object is serialized. To use the `simplejson` module, simply call `simplejson.dumps()` on the object you want to convert.

```python
import simplejson

my_object = {
    'name': 'John Doe',
    'age': 42
}

json_string = simplejson.dumps(my_object)

print(json_string)
# '{"name": "John Doe", "age": 42}'
```

## Using the Jsonpickle Module

The `jsonpickle` module is a fourth way to convert a Python object into a JSON string. The `jsonpickle` module is useful if you need to preserve the structure of the object, including any custom classes. To use the `jsonpickle` module, simply call `jsonpickle.encode()` on the object you want to convert.

```python
import jsonpickle

my_object = {
    'name': 'John Doe',
    'age': 42
}

json_string = jsonpickle.encode(my_object)

print(json_string)
# '{"py/object": "__main__.MyObject", "name": "John Doe", "age": 42}'
```
