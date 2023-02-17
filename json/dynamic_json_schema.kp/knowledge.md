---
title: Schema for JSON with unspecified property names
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: JSON Schema allows for the definition of unknown properties through the use of the `additionalProperties` keyword.
---

**Contents**

[TOC]

##### Solution 1: 
Using the `patternProperties` keyword:

The `patternProperties` keyword allows you to define a schema for a set of properties with matching names. It takes an object, where each key is a regular expression pattern and each value is a schema that will be applied to any properties with names matching the pattern.

For example, if you wanted to define a schema for any properties beginning with `foo_`, you could use the following:

```json
{
  "patternProperties": {
    "^foo_.*": {
      "type": "string"
    }
  }
}
```

##### Solution 2: 
Using the `additionalProperties` keyword:

The `additionalProperties` keyword allows you to define a schema for any properties with names that are not explicitly defined in the properties or patternProperties keywords. It takes a boolean or an object as its value.

If the value is a boolean, it will either allow (true) or disallow (false) additional properties.

If the value is an object, it will be used as a schema for any additional properties.

For example, if you wanted to allow any additional properties, but ensure they are all strings, you could use the following:

```json
{
  "additionalProperties": {
    "type": "string"
  }
}
```
