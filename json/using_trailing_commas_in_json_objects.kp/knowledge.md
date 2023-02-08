---
title: Is it possible to include a comma after the last item in a JSON object?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, a trailing comma is allowed in a JSON object.
---

**Contents**

[TOC]

Yes

## Syntax

Trailing commas are allowed in JSON objects, as long as the last element does not have a trailing comma.

## Example

The following is an example of a valid JSON object with a trailing comma:

```
{
    "name": "John Smith",
    "age": 30,
    "address": "123 Main Street",
    "city": "New York",
    "state": "NY",
    "zip": 10001,
}
```

## Limitations

The trailing comma is not allowed in the last element of a JSON object. The following is an example of an invalid JSON object with a trailing comma:

```
{
    "name": "John Smith",
    "age": 30,
    "address": "123 Main Street",
    "city": "New York",
    "state": "NY",
    "zip": 10001,
}
```
