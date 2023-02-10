---
title: Converting a Python namedtuple to a JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: It is possible to serialize a Python namedtuple to JSON using the json.dumps() method.
---

**Contents**

[TOC]

##### Serializing a Python namedtuple to json

1. Using `json.dumps()`:
   The `json.dumps()` method can be used to serialize a Python namedtuple to json. This method takes the namedtuple as an argument and returns a JSON string.

2. Using `jsonpickle`:
   The `jsonpickle` library can be used to serialize a Python namedtuple to json. This library provides a `dumps()` method that takes the namedtuple as an argument and returns a JSON string.

3. Using `dict`:
   A Python namedtuple can also be serialized to json by converting it to a `dict` object. This can be done by using the `_asdict()` method of the namedtuple. The `dict` object can then be serialized to json using the `json.dumps()` method.

4. Using `collections.namedtuple()`:
   The `collections.namedtuple()` method can be used to create a namedtuple from a `dict` object. This `dict` object can then be serialized to json using the `json.dumps()` method.
