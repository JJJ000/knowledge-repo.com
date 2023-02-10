---
title: Define a property within a JSON schema that can accept either a string or null value
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: A string or null value can be specified with the `type` keyword in JSON Schema, e.g. `type` [`string`, `null`].
---

**Contents**

[TOC]

## Syntax

```
{
  "type": ["string", "null"]
}
```

## Explanation

The JSON Schema above specifies that the value can be either a string or null. This is accomplished by using an array with two elements, "string" and "null". This tells the validator that the value must be either a string or null.

## Example

The following JSON is valid according to the schema:

```
{
  "value": "Hello World"
}
```

The following JSON is also valid:

```
{
  "value": null
}
```
