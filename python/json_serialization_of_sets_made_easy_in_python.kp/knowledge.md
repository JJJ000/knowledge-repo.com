---
title: What is the method for JSON serializing sets?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Sets cannot be directly JSON serialized in Python, they need to be converted into a list or another JSON serializable format first.
---

**Contents**

[TOC]

Section 1: Introduction to JSON Serialization in Python
JSON (JavaScript Object Notation) is a lightweight data interchange format that is easy for humans to read and write and easy for machines to parse and generate. Python has a built-in `json` module that provides a convenient way to encode and decode JSON data.

JSON serialization is the process of converting Python objects into JSON strings that can be stored or transmitted over the network. However, not all Python objects can be serialized by the `json` module, including sets.

In this tutorial, we will explore how to JSON serialize sets in Python.

Section 2: Converting a Set to a List
The `json` module can serialize lists, so one way to JSON serialize a set is to convert it to a list first using the `list()` function. Here's an example:

```
import json

my_set = {1, 2, 3}

serialized = json.dumps(list(my_set))

print(serialized)
# Output: "[1, 2, 3]"
```

In this example, we convert the set `my_set` to a list using the `list()` function, and then use the `json.dumps()` function to serialize the list to a JSON string. The output is the JSON string `"[1, 2, 3]"`.

Section 3: Using a Custom Encoder
Another way to JSON serialize sets in Python is to use a custom JSON encoder that handles sets as a special case. We can create a custom encoder by subclassing the `json.JSONEncoder` class and overriding its `default()` method.

Here's an example:

```
import json

class SetEncoder(json.JSONEncoder):
    def default(self, obj):
        if isinstance(obj, set):
            return list(obj)
        return json.JSONEncoder.default(self, obj)

my_set = {1, 2, 3}

serialized = json.dumps(my_set, cls=SetEncoder)

print(serialized)
# Output: "[1, 2, 3]"
```

In this example, we define a custom `SetEncoder` class that overrides the `default()` method to handle sets as a special case. If the object is a set, we convert it to a list using the `list()` function, and call the `default()` method of the parent class to serialize the list.

We then create a JSON string from the `my_set` set using the `json.dumps()` function and passing our custom encoder to the `cls` parameter. The output is the JSON string `"[1, 2, 3]"`.

Section 4: Conclusion
In conclusion, we have explored two ways to JSON serialize sets in Python: by converting them to a list first, or by using a custom JSON encoder that handles sets as a special case. Both approaches are valid and can be used depending on the specific requirements of your project.
