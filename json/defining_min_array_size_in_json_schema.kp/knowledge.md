---
title: What is the minimum number of elements in an array according to the JSON schema?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: The minimum size of an array can be defined using the `minItems` keyword in the JSON schema.
---

**Contents**

[TOC]

1. **Define the Array**

The first step in defining the min size of an array in a JSON schema is to define the array itself. This can be done by specifying the "type" as "array" and adding the "items" property to the schema. The "items" property contains a schema that defines the type of items that are allowed in the array.

2. **Specify the Minimum Size**

The next step is to specify the minimum size for the array. This can be done by adding the "minItems" property to the schema and setting the value to the desired minimum size.

3. **Specify the Maximum Size**

The third step is to specify the maximum size for the array. This can be done by adding the "maxItems" property to the schema and setting the value to the desired maximum size.

4. **Validate the Array**

The final step is to validate the array to ensure that the minimum and maximum sizes are enforced. This can be done by using a JSON Schema validator to check the array against the schema.
