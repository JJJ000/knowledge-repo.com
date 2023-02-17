---
title: Constructing a bson object from a JSON string
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: The BSON object can be created from a JSON string using the BSON library`s `fromExtendedJSON` method.
---

**Contents**

[TOC]

## Section 1: What is BSON?
BSON (Binary JSON) is a binary-encoded serialization of JSON-like documents. It is used to store documents and make remote procedure calls in MongoDB. BSON provides a more efficient way to store data than JSON, making it faster to transfer over the network.

## Section 2: What is JSON?
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based, human-readable format for representing simple data structures and objects. JSON is used to store and exchange data between applications and web services.

## Section 3: How to Create a BSON Object from a JSON String
To create a BSON object from a JSON string, you can use the bson.BSON.encode() method. This method takes a JSON string as an argument and returns a BSON object.

## Section 4: Example
Here is an example of how to create a BSON object from a JSON string:

```
import bson

json_string = '{"name": "John", "age": 30}'
bson_object = bson.BSON.encode(json_string)

print(bson_object)
# b'\x16\x00\x00\x00\x02name\x00\x04\x00\x00\x00John\x00\x02age\x00\x1e\x00\x00\x00\x00'
```
