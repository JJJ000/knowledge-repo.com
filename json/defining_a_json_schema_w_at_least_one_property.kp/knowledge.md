---
title: What is the syntax for a JSON schema that requires at least one of multiple properties?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: A JSON schema can require at least one of many properties by using the `anyOf` keyword.
---

**Contents**

[TOC]

**Section 1: Defining the Schema**

A JSON schema is a document that defines the structure of a JSON object. It can be used to validate that a JSON document conforms to a certain structure and contains the required fields.

The following example shows how to define a JSON schema that requires at least one of many properties:

```json
{
    "$schema": "http://json-schema.org/draft-07/schema#",
    "type": "object",
    "properties": {
        "property1": {
            "type": "string"
        },
        "property2": {
            "type": "string"
        },
        "property3": {
            "type": "string"
        }
    },
    "required": ["property1", "property2", "property3"],
    "minProperties": 1
}
```

**Section 2: Explaining the Schema**

The schema defines an object type with three properties (property1, property2, and property3). The `required` keyword is used to indicate that all three properties must be present in the JSON document. The `minProperties` keyword is used to indicate that at least one of the properties must be present in the JSON document.

**Section 3: Testing the Schema**

The following example shows a valid JSON document that conforms to the schema:

```json
{
    "property1": "value1",
    "property2": "value2"
}
```

The following example shows an invalid JSON document that does not conform to the schema:

```json
{
    "property4": "value4"
}
```

**Section 4: Further Reading**

For more information about JSON schemas, see the official documentation at http://json-schema.org/.
