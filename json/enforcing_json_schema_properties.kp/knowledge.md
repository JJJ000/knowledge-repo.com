---
title: Only accept properties that have been defined in the JSON schema
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Only properties declared in the JSON schema will be allowed in the JSON.
---

**Contents**

[TOC]

## Validation

JSON schema can be used to validate the structure of a JSON object. This means that only properties that are declared in the JSON schema will be allowed in the JSON object.

## Parsing

The JSON parser can be configured to only allow properties that are declared in the JSON schema. This ensures that no invalid properties are present in the JSON object.

## Error Handling

When a property is encountered that is not declared in the JSON schema, an error can be thrown. This ensures that invalid properties are not present in the JSON object.

## Security

Using JSON schema to validate JSON objects can also provide an additional layer of security. By only allowing properties that are declared in the JSON schema, it can help to prevent malicious data from being present in the JSON object.
