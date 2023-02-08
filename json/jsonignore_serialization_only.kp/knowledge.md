---
title: Only applying @jsonignore when serializing, but not when deserializing
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: @JsonIgnore can be used to prevent a property from being serialized, but it will still be deserialized.
---

**Contents**

[TOC]

## Deserialization

When deserializing, @JsonIgnore is ignored. This means that any field marked with @JsonIgnore will be deserialized as normal, and the value of the field will be set to the value of the corresponding JSON property.

## Serialization

When serializing, @JsonIgnore is respected. This means that any field marked with @JsonIgnore will not be included in the resulting JSON, and the value of the field will not be serialized.
