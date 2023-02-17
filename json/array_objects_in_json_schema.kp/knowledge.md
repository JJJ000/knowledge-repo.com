---
title: A JSON schema describing an array of objects
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: An array of objects can be defined using a JSON Schema with the type set to `array` and the `items` keyword set to an object schema definition.
---

**Contents**

[TOC]

## Section 1: Overview
A JSON Schema definition for an array of objects is a definition that describes an array containing zero or more objects. An object is a collection of key-value pairs. Each key-value pair is an attribute-value pair.

## Section 2: Syntax
The syntax for a JSON Schema definition for an array of objects is as follows:

```
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "array",
  "items": {
    "type": "object",
    "properties": {
      "attribute1": {
        "type": "data-type"
      },
      "attribute2": {
        "type": "data-type"
      },
      ...
    },
    "required": [
      "attribute1",
      "attribute2",
      ...
    ]
  }
}
```

## Section 3: Example
For example, a JSON Schema definition for an array of objects with two attributes, `name` (string) and `age` (integer), could be written as follows:

```
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "array",
  "items": {
    "type": "object",
    "properties": {
      "name": {
        "type": "string"
      },
      "age": {
        "type": "integer"
      }
    },
    "required": [
      "name",
      "age"
    ]
  }
}
```

## Section 4: Validation
The JSON Schema definition for an array of objects can be used to validate an array of objects. If an array of objects does not conform to the schema definition, then it is considered invalid.
