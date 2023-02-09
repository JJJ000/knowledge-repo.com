---
title: Does JSON begin with "["?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, JSON can start with `[` as it is used to denote the start of an array.
---

**Contents**

[TOC]

## Yes

JSON can start with a `[` character. This indicates that the JSON is an array, which is a collection of values (like a list). An array is enclosed in square brackets and each value is separated by a comma.

## Example

An example of JSON starting with a `[` would be:

```
[
  {
    "name": "John Doe",
    "age": 30
  },
  {
    "name": "Jane Doe",
    "age": 28
  }
]
```

## Usage

JSON arrays are commonly used to store a collection of related data, such as a list of objects or a list of values. They can also be used to represent a set of instructions or a set of data that needs to be processed in a specific order.

## Syntax

When writing JSON that starts with a `[`, it is important to remember that the opening `[` must have a matching closing `]` at the end of the JSON. Furthermore, each value in the array must be separated by a comma.
