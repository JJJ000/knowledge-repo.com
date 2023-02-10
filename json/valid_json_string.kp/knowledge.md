---
title: Is this plain text considered to be valid JSON format?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: No, this is not valid JSON.
---

**Contents**

[TOC]

## Yes

JSON (JavaScript Object Notation) is a text-based format for representing structured data, and is widely used for data interchange in web applications. A valid JSON string must adhere to the following rules:

1. The string must begin and end with double quotation marks.
2. The data must be in name/value pairs, separated by a colon.
3. The data must be separated by commas.
4. The data must be enclosed in curly brackets.

This simple string is considered valid JSON because it adheres to all four rules:

```
"name": "John Doe"
```

## No

However, this simple string is not considered valid JSON because it is not an object. JSON objects are composed of key-value pairs, and this string only contains a single key-value pair. A valid JSON object must contain at least two key-value pairs. For example:

```
{
  "name": "John Doe",
  "age": 30
}
```
