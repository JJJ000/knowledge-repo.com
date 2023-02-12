---
title: Json schema  "additionalproperties" with "allof"
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: The `allof` keyword can be used in conjunction with the `additionalProperties` keyword to specify that an object must validate against all given schemas and any additional properties must also validate against the given schema.
---

**Contents**

[TOC]

**Section 1: Introduction**

JSON Schema is a standard for describing the structure of a JSON document. It provides a way to validate that a given JSON document is valid according to the schema. The "allof" keyword is used in JSON Schema to indicate that all of the subschemas in the array must be valid for the document to be valid. The "additionalProperties" keyword is used to indicate that any additional properties beyond those specified in the schema should be allowed.

**Section 2: The "allof" Keyword**

The "allof" keyword is used in JSON Schema to indicate that all of the subschemas in the array must be valid for the document to be valid. This means that all of the subschemas must be satisfied for the document to be considered valid. For example, if the schema contains two subschemas, then both subschemas must be satisfied for the document to be valid.

**Section 3: The "additionalProperties" Keyword**

The "additionalProperties" keyword is used to indicate that any additional properties beyond those specified in the schema should be allowed. This means that if the schema contains a list of properties, then any additional properties beyond those listed are allowed. For example, if the schema contains a list of properties A, B, and C, then any additional properties beyond A, B, and C are allowed.

**Section 4: Combining "allof" and "additionalProperties"**

When combining the "allof" and "additionalProperties" keywords, all of the subschemas must be satisfied, and any additional properties beyond those specified in the schema are allowed. This means that all of the subschemas must be satisfied, but any additional properties beyond those specified are allowed. For example, if the schema contains two subschemas and a list of properties A, B, and C, then all of the subschemas must be satisfied, and any additional properties beyond A, B, and C are allowed.
