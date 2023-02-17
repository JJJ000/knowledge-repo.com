---
title: Using the json.dumps() method to encode bytes in JSON is resulting in a typeerror
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Use the json.dumps() method with the `ensure\_ascii` argument set to False.
---

**Contents**

[TOC]

## Encoding Bytes in JSON
JSON is a data-interchange format that is used to store and exchange data. It is a text-based, human-readable format that can represent simple data structures and objects. JSON can represent four primitive types (strings, numbers, booleans, and null) and two structured types (objects and arrays).

It is possible to encode bytes in JSON using the `base64` encoding format. This encoding format is used to represent binary data in an ASCII string format by translating it into a radix-64 representation.

## Using json.dumps()
The `json.dumps()` method is used to convert a Python object into a JSON string. This method takes an object as an argument and returns a JSON string representation of the object.

The `json.dumps()` method can be used to encode bytes in JSON, but it is important to note that the bytes must first be encoded in the `base64` format before being passed to the `json.dumps()` method.

## Handling a TypeError
When using the `json.dumps()` method to encode bytes in JSON, it is possible to encounter a `TypeError` if the bytes have not been properly encoded. This error occurs when the `json.dumps()` method is passed a non-string object.

To resolve this issue, the bytes must first be encoded in the `base64` format before being passed to the `json.dumps()` method. After the bytes have been encoded, the `json.dumps()` method can be used to convert the encoded bytes into a JSON string.

## Conclusion
It is possible to encode bytes in JSON using the `base64` encoding format and the `json.dumps()` method. If a `TypeError` is encountered when using the `json.dumps()` method, it is likely that the bytes have not been properly encoded and must first be encoded in the `base64` format before being passed to the `json.dumps()` method.
