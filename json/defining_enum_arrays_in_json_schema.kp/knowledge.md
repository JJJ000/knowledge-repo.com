---
title: The correct way to define an array of enumerated values in a JSON schema is by using the "enum" keyword
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: An array of enums can be defined in JSON schema using the `enum` keyword within the array definition.
---

**Contents**

[TOC]

### Section 1: Declaring the Enum Values

The first step in defining an array of enums in JSON schema is to declare the enum values that will be used. This can be done by using the `enum` keyword and providing an array of values. For example: 

```
"enum": ["value1", "value2", "value3"]
```

### Section 2: Declaring the Array

The next step is to declare the array itself. This can be done using the `type` keyword, followed by the `array` keyword. For example:

```
"type": "array"
```

### Section 3: Declaring the Array Items

The third step is to declare the items in the array. This can be done by using the `items` keyword and providing the enum values as an array. For example:

```
"items": {
    "enum": ["value1", "value2", "value3"]
}
```

### Section 4: Combining the Declaration

The final step is to combine the declarations into a single JSON schema. For example:

```
{
    "type": "array",
    "items": {
        "enum": ["value1", "value2", "value3"]
    }
}
```
