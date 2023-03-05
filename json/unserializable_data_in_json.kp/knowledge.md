---
title: Cannot be transformed into a JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Data types such as sets and complex numbers are not JSON serializable by default in Python.
---

**Contents**

[TOC]

JSON Serialization
------------------------

JSON serialization is the process of converting a Python object into a JSON string. This is done using the `json.dumps` function. Most Python objects can be serialized into JSON without any issues. However, there are certain data types that cannot be serialized.

Non-serializable Data Types
------------------------

The following data types cannot be serialized into JSON:

- Sets
- Complex Numbers
- Functions
- Lambda Functions
- Generators

For example, if we try to serialize a set using `json.dumps`, we will get a `TypeError`:

``` python
import json

my_set = {1, 2, 3, 4, 5}

json.dumps(my_set)
```

Output:
```
TypeError: Object of type 'set' is not JSON serializable
```

Serialization of Custom Objects
-------------------------

In addition to the above, custom objects created by users also cannot be serialized by default. The `json.dumps` function can only serialize built-in data types. If a custom object needs to be serialized, it's necessary to serialize it manually by defining a custom encoder using the `json.JSONEncoder` class.

For example, suppose we have a custom class named `Person`.

``` python
import json

class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

p = Person("John", 30)
```

If we try to serialize this object using `json.dumps`, we will get an error:

``` python
json.dumps(p)
```

Output:
```
TypeError: Object of type 'Person' is not JSON serializable
```

To serialize the `Person` object above, we can create a custom encoder using the `json.JSONEncoder` class. We can override the `default` method in this class to convert the `Person` object into a serializable format.

``` python
class PersonEncoder(json.JSONEncoder):
    def default(self, o):
        return {'name': o.name, 'age': o.age}

p_json = json.dumps(p, cls=PersonEncoder)

print(p_json)
```

Output:
```
{"name": "John", "age": 30}
```

Now, our `Person` object has been successfully serialized into a JSON string.
