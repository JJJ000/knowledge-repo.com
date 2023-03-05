---
title: Revisiting the practice of utilizing designated words as names for properties
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Using reserved words as property names in Json can be avoided by enclosing the property name in quotes or by escaping the character.
---

**Contents**

[TOC]

Section 1: What are reserved words in programming?

Reserved words are special keywords in a programming language that have a predefined meaning and cannot be used as identifiers, such as variable or function names. These words are reserved by the language specification and are used to describe specific syntax elements or operations within the code.

Section 2: How are reserved words used in JSON?

In JSON, reserved words are not allowed to be used as property names. This is because JSON property names must be valid strings, and reserved words are not valid as they are already reserved for specific meanings in the language.

For example, the following JSON is invalid because "true" is a reserved word and cannot be used as a property name:

```json
{
  "true": "value"
}
```

To avoid this issue, you can simply rename the property using a different name that is not a reserved word. For example:

```json
{
  "isTrue": "value"
}
```

Section 3: What are the implications of using reserved words in JSON?

Using reserved words as property names can cause parse errors and syntax issues, as it goes against the JSON specification. It can also make the code more difficult to read and understand.

In addition, using reserved words as property names can cause issues when converting JSON to other datatypes, such as JavaScript objects. In JavaScript, reserved words can be used as property names, but this is not possible in JSON.

Section 4: Conclusion

In conclusion, it is recommended that reserved words not be used as property names in JSON, as it goes against the specification and can cause issues with parsing and conversion. Instead, choose a different, unreserved name to ensure that the JSON is valid and easily interoperable with other systems.
