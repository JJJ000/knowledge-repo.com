---
title: Creating a string representation of a value with json_encode() and escaping the forward slashes
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, json\_encode() escapes forward slashes by default.
---

**Contents**

[TOC]

## Problem

JSON encoding is a process that converts data into a string format that is readable by machines. This string is based on the JavaScript Object Notation (JSON) format, which is a standardized way of representing data. However, when encoding a string, there are certain characters that may be escaped in order to ensure the string is valid JSON. One of these characters is the forward slash (`/`).

## Explanation

A forward slash (`/`) is a special character in JSON, which is used to separate elements in an object or array. For example, in a JSON object, the forward slash is used to separate the key and value of each property. As such, the forward slash needs to be escaped in order for the JSON string to be valid.

When encoding a string, the JSON encoder will escape any forward slashes by adding an additional forward slash before it. This ensures that the forward slash is treated as a literal character instead of a separator.

## Examples

Consider the following JSON string:

```json
{
  "name": "John Doe",
  "age": 30
}
```

When encoded, the string will be escaped and the forward slash will be escaped as well:

```json
{
"name": "John Doe",
"age": 30
}
```

## Conclusion

JSON encoding is a process that converts data into a string format that is readable by machines. The JSON encoder will escape any forward slashes by adding an additional forward slash before it in order to ensure the string is valid JSON. This ensures that the forward slash is treated as a literal character instead of a separator.
