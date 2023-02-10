---
title: Parsing JSON with gson using enumerated types
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Enums can be used as a type adapter to deserialize JSON strings into corresponding enum values when parsing JSON with GSON.
---

**Contents**

[TOC]

### Section 1: Overview
Enums are a powerful tool for representing a fixed set of values in a type-safe way. When using GSON to parse JSON, enums can be used to represent the values of certain fields in the JSON. This allows GSON to automatically convert the JSON into the corresponding enum type.

### Section 2: Defining the Enum
To use enums with GSON, the enum must be defined in the code. This is done by creating a class that extends the `Enum` class, and adding a list of enum values. For example, to define a `Color` enum:

```
public enum Color {
    RED,
    GREEN,
    BLUE
}
```

### Section 3: Parsing with GSON
When GSON parses a JSON object, it will automatically try to match the field values to the corresponding enum values. For example, if the JSON contains a field `color` with the value `"RED"`, GSON will automatically convert it to the `Color.RED` enum.

### Section 4: Custom Deserializers
In some cases, the JSON field values may not match the enum values exactly. In these cases, a custom deserializer can be used to convert the JSON field values to the corresponding enum values. For example, if the JSON contains a field `color` with the value `"red"`, a custom deserializer can be used to convert it to the `Color.RED` enum.
