---
title: Check if a deserialized object is missing a field using the jsonconvert class in json.net
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: No, JsonConvert cannot detect if a deserialized object is missing a field.
---

**Contents**

[TOC]

## Deserialization

The JsonConvert class in Json.NET provides methods for deserializing JSON text into objects. The `DeserializeObject` method can be used to deserialize a JSON string into a strongly typed object.

## Checking for Missing Fields

When deserializing a JSON string into an object, it is possible to detect if any of the fields are missing. This can be done by using the `ValidateObject` method of the `JsonConvert` class. This method takes an object and a `JsonSerializerSettings` object as parameters. In the `JsonSerializerSettings` object, the `MissingMemberHandling` property can be set to `Error` which will cause an exception to be thrown if any of the fields are missing.

## Handling Missing Fields

If the `MissingMemberHandling` property is set to `Ignore`, then the fields that are missing will simply be ignored and the deserialization will be successful.

## Summary

The JsonConvert class in Json.NET provides methods for deserializing JSON text into objects. It is possible to detect if any of the fields are missing by using the `ValidateObject` method and setting the `MissingMemberHandling` property in the `JsonSerializerSettings` object to `Error`. If the `MissingMemberHandling` property is set to `Ignore`, then the fields that are missing will simply be ignored and the deserialization will be successful.
