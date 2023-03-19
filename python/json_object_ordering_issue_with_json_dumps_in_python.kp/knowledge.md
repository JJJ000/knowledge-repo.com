---
title: Is it possible to use "json.dumps" to re-order the items in a JSON object?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Yes, JSON object keys may appear in a different order than the input order when using `json.dumps` in Python.
---

**Contents**

[TOC]

## Problem description
When a JSON object is created and printed using the `json.dumps` method in Python, the order of items in the object might not be the same as the order in which they were added to the object.

## Explanation
JSON stands for JavaScript Object Notation, and it is a format for storing and transporting data. A JSON object is an unordered set of key-value pairs, where the keys are strings and the values are any JSON values, including arrays and other JSON objects. When using the `json.dumps` method in Python, the order of items in the resulting string representation of the JSON object may not be the same as the order in which the items were added to the original object. This is because the order of items in a JSON object is not significant and is not preserved by the serialization process.

## Example
Consider the following example:

```python
import json
    
data = {
    "name": "John Doe",
    "age": 42,
    "address": {
        "street": "123 Main St",
        "city": "Anytown",
        "state": "CA",
        "zip": "12345"
    },
    "phone_numbers": ["555-1234", "555-5678"]
}

print(json.dumps(data))
```

The output of this program might be:

```json
{"phone_numbers": ["555-1234", "555-5678"], "name": "John Doe", "address": {"zip": "12345", "city": "Anytown", "street": "123 Main St", "state": "CA"}, "age": 42}
```

Notice that the items in the resulting JSON string are not in the same order as the items in the original `data` object.

## Solution
If you need to preserve the order of items in a JSON object, you can use the `collections.OrderedDict` class in Python instead of a regular dictionary. This class maintains the order of items as they are added to the dictionary. Here's an example:

```python
import json
from collections import OrderedDict
    
data = OrderedDict([
    ("name", "John Doe"),
    ("age", 42),
    ("address", OrderedDict([
        ("street", "123 Main St"),
        ("city", "Anytown"),
        ("state", "CA"),
        ("zip", "12345")
    ])),
    ("phone_numbers", ["555-1234", "555-5678"])
])

print(json.dumps(data))
```

The output of this program will be:

```json
{"name": "John Doe", "age": 42, "address": {"street": "123 Main St", "city": "Anytown", "state": "CA", "zip": "12345"}, "phone_numbers": ["555-1234", "555-5678"]}
```

Notice that the order of items in the resulting JSON string is the same as the order of items in the original `data` object.

Another solution is to use the `sort_keys` parameter of `json.dumps` to sort the keys of the JSON object alphabetically. This will not preserve the original order of items, but it will make the output consistent across multiple runs of the program. Here's an example:

```python
import json
    
data = {
    "name": "John Doe",
    "age": 42,
    "address": {
        "street": "123 Main St",
        "city": "Anytown",
        "state": "CA",
        "zip": "12345"
    },
    "phone_numbers": ["555-1234", "555-5678"]
}

print(json.dumps(data, sort_keys=True))
```

The output of this program will be:

```json
{"address": {"city": "Anytown", "state": "CA", "street": "123 Main St", "zip": "12345"}, "age": 42, "name": "John Doe", "phone_numbers": ["555-1234", "555-5678"]}
```

Notice that the keys of the items in the resulting JSON string are sorted alphabetically.
