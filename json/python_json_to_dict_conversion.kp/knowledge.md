---
title: Transform a JSON string into a dictionary using python
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Using Python, you can convert a JSON string to a dictionary by using the json.loads() method.
---

**Contents**

[TOC]

## Section 1: Parsing JSON Strings
Parsing a JSON string is a common task in Python that can be accomplished using the `json` module. The `json.loads()` function can be used to parse a JSON string into a dictionary.

## Section 2: Syntax
The syntax for parsing a JSON string into a dictionary is as follows:
```
dict_object = json.loads(json_string)
```

## Section 3: Example
For example, the following JSON string can be parsed into a dictionary using `json.loads()`:
```
json_string = '{"name": "John", "age": 30, "city": "New York"}'

dict_object = json.loads(json_string)
```

## Section 4: Output
The resulting dictionary object will look like this:
```
{
    "name": "John",
    "age": 30,
    "city": "New York"
}
```
