---
title: Serializing a decimal object into a JSON format using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The Decimal object must be converted to a string before it can be serialized with JSON.
---

**Contents**

[TOC]

# Serialize Decimal Object
The Decimal object can be serialized using the json.dumps() function.

## json.dumps()
The json.dumps() function converts a Python object into a JSON string. It takes an object as its argument and returns a JSON string.

## Decimal Object
The Decimal object is a Python object that represents a decimal number. It is used to represent exact values, such as currency values.

## Serializing Decimal Object
To serialize a Decimal object, we can use the json.dumps() function with the default argument, which is the Decimal class. This will convert the Decimal object into a JSON string.

## Example
```
import json
from decimal import Decimal

value = Decimal('1.2345')

json_string = json.dumps(value)

print(json_string)

# Output: "1.2345"
```
