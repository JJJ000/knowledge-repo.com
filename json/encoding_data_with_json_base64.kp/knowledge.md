---
title: Convert a base64 encoded data into a JSON string
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: A base64 encoded data can be serialized in JSON by encoding it as a string.
---

**Contents**

[TOC]

**Section 1: Encoding**

Base64 encoding is a way of representing binary data in an ASCII string format. It is typically used when there is a need to encode binary data that needs to be stored and transferred over media that are designed to deal with textual data. 

**Section 2: JSON**

JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based, human-readable format for representing simple data structures and associative arrays (called objects).

**Section 3: Serializing Data**

To serialize base64 encoded data in JSON, you need to first encode the data using the base64 encoding algorithm. Then, the encoded data can be stored in a JSON object as a string.

**Section 4: Example**

For example, let's say we have a base64 encoded string `"SGVsbG8gV29ybGQ="`. To store this in a JSON object, we can do the following:

```json
{
    "data": "SGVsbG8gV29ybGQ="
}
```
