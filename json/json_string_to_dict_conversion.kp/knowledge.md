---
title: Transforming a JSON string into a dictionary, not an array
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the json.loads() method to convert a JSON string to a dictionary.
---

**Contents**

[TOC]

### Section 1: Overview

JSON (JavaScript Object Notation) is a data-interchange format used for exchanging information between a client and a server. It is a lightweight format that is used to store and transport data. It is easy for humans to read and write, and for machines to parse and generate. JSON is composed of two structures: a collection of name/value pairs and an ordered list of values.

### Section 2: Converting JSON String to Dictionary

The process of converting a JSON string to a dictionary involves using the built-in JSON library. The JSON library can be used to parse a JSON string and convert it into a dictionary. The dictionary can then be used to access the values stored in the JSON string.

### Section 3: Accessing Values

Once the JSON string has been converted to a dictionary, the values can be accessed using the keys. The keys are strings that represent the name of the value. The values can then be accessed using the keys.

### Section 4: Example

For example, given the following JSON string: 

```
{
    "name": "John",
    "age": 25,
    "address": "123 Main Street"
}
```

The dictionary can be created using the JSON library: 

```
import json

json_string = '{"name": "John", "age": 25, "address": "123 Main Street"}'

data = json.loads(json_string)
```

The values can then be accessed using the keys: 

```
name = data["name"]
age = data["age"]
address = data["address"]
```
