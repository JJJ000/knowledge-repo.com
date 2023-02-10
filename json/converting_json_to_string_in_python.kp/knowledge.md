---
title: Transforming a JSON object into a string in python
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: In Python, JSON can be converted to a string using the json.dumps() function.
---

**Contents**

[TOC]

# Section 1: Serializing JSON

Serializing JSON means converting a JSON object into a string. This is done by using the json.dumps() method. The json.dumps() method takes a Python object and converts it into a string.

# Section 2: json.dumps() Syntax

The syntax for the json.dumps() method is as follows:

json.dumps(obj, skipkeys=False, ensure_ascii=True, check_circular=True, allow_nan=True, cls=None, indent=None, separators=None, default=None, sort_keys=False, **kwargs)

# Section 3: Example

Here is an example of how to use the json.dumps() method:

import json

# a Python object (dict):
x = {
  "name": "John",
  "age": 30,
  "city": "New York"
}

# convert into JSON:
y = json.dumps(x)

# the result is a JSON string:
print(y)

# Section 4: Output

The output of the above code will be:

{"name": "John", "age": 30, "city": "New York"}
