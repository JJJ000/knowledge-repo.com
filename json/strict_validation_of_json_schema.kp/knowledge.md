---
title: Rephrased the validation of JSON schema must restrict the existence of fields apart from the ones specified in the schema
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A JSON Schema validation can be set up to not allow fields other than those declared in the schema by using the `additionalProperties` property and setting it to `false`.
---

**Contents**

[TOC]

## Introduction
JSON (JavaScript Object Notation) Schema is a vocabulary that allows developers to validate the structure and data types of JSON objects. It provides a way to specify what values are expected for each field and how the fields relate to each other. One common requirement in JSON schema validation is to not allow any fields other than those declared in the schema.

## Why not allow extra fields?
Preventing extra fields in JSON objects can help maintain data consistency and prevent unexpected behavior in applications. If extra fields are allowed, it could lead to problems like data corruption and difficulty in debugging. In addition, it could violate data privacy and security policies if sensitive information is inadvertently included.

## How to prevent extra fields
To prevent fields other than those declared in the JSON schema, the `additionalProperties` keyword can be set to `false`. This keyword specifies whether additional fields not defined in the schema are allowed in the JSON object. When `additionalProperties` is set to `false`, any fields not defined in the schema will cause a validation error.

For example, if we have a JSON schema that looks like this:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "name": {
      "type": "string"
    },
    "age": {
      "type": "integer"
    }
  },
  "additionalProperties": false
}
```

This schema defines two fields, `name` and `age`. The `additionalProperties` keyword is set to `false`, meaning that any extra fields will be considered invalid.

## Benefits of preventing extra fields
By preventing extra fields in JSON objects, we can ensure that the data is consistent with the schema and that no sensitive information is included. This can help improve application reliability, maintainability, and security. In addition, it can make it easier to debug issues by reducing the number of potential sources of error.
