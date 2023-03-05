---
title: Methods for obtaining string objects in place of unicode from json
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Use the `json.loads` method to load the JSON data and pass the `encoding=`string`` parameter to convert Unicode objects to string objects.
---

**Contents**

[TOC]

## Introduction

JSON is a widely used data format to exchange data across different platforms. It is very common to work with JSON data in Python because of the JSON library provided in the Python standard library. However, when reading JSON data, the strings are returned as Unicode objects by default. In some cases, we may need to get string objects instead of Unicode objects. In this article, we will discuss how to get string objects instead of Unicode from JSON in Python.

## Using the `object_hook` parameter of the `json.loads()` function

The `json.loads()` function is used to parse JSON data in Python. One way to get string objects instead of Unicode objects is by using the `object_hook` parameter of the `json.loads()` function. This parameter is a function that can modify the object before it is returned. We can define a function that will be called for every object parsed from the JSON data. In this function, we can check if the object is a Unicode object and convert it to a string object if necessary.

```python
import json

def custom_decoder(obj):
    if isinstance(obj, str):
        return str(obj)
    return obj

json_data = '{"name": "John Doe", "age": 30 }'
data = json.loads(json_data, object_hook=custom_decoder)
print(type(data["name"]))
```

In the above example, we define a `custom_decoder` function that checks if the object is a Unicode object and converts it to a string object if necessary. Then, we pass this function as the `object_hook` parameter to the `json.loads()` function. When we print the type of the `name` value, we get `<class 'str'>` which shows that it is a string object.

## Using the `json.JSONDecoder` class

Another way to get string objects instead of Unicode objects is by using the `json.JSONDecoder` class. This class can be used to customize the decoding process of JSON data. We can define our own decoding function that will be called for every object parsed from the JSON data. In this function, we can convert the Unicode object to a string object if necessary.

```python
import json

class CustomDecoder(json.JSONDecoder):
    def decode(self, json_string):
        result = super().decode(json_string)
        return self._decode(result)

    def _decode(self, obj):
        if isinstance(obj, str):
            return str(obj)
        elif isinstance(obj, dict):
            return {self._decode(key): self._decode(val) for key, val in obj.items()}
        elif isinstance(obj, list):
            return [self._decode(elem) for elem in obj]
        else:
            return obj

json_data = '{"name": "John Doe", "age": 30 }'
data = json.loads(json_data, cls=CustomDecoder)
print(type(data["name"]))
```

In the above example, we define a `CustomDecoder` class that overrides the `decode` method of the `json.JSONDecoder` class. In this method, we first call the `decode` method of the parent class to get the decoded object. Then, we call a private method `_decode` to convert the Unicode object to a string object if necessary. Finally, we return the converted object. When we pass an instance of the `CustomDecoder` class as the `cls` parameter to the `json.loads()` function, we get string objects instead of Unicode objects.

## Using the `ensure_ascii` parameter of the `json.dumps()` function

When we serialize Python objects to JSON using the `json.dumps()` function, the strings are represented as Unicode objects by default. One way to get string objects instead of Unicode objects is by using the `ensure_ascii` parameter of the `json.dumps()` function. If we set this parameter to False, the strings will be represented as string objects in the resulting JSON data.

```python
import json

data = {"name": "John Doe", "age": 30 }
json_data = json.dumps(data, ensure_ascii=False)
print(type(json.loads(json_data)["name"]))
```

In the above example, we define a Python dictionary object `data` and serialize it to JSON using the `json.dumps()` function with the `ensure_ascii` parameter set to False. When we parse the resulting JSON data using the `json.loads()` function and print the type of the `name` value, we get `<class 'str'>` which shows that it is a string object.

## Conclusion

In this article, we discussed how to get string objects instead of Unicode from JSON in Python. We discussed three different methods to achieve this: using the `object_hook` parameter of the `json.loads()` function, using the `json.JSONDecoder` class, and using the `ensure_ascii` parameter of the `json.dumps()` function. Depending on the scenario, we can choose the appropriate method to get string objects instead of Unicode objects from JSON in Python.
