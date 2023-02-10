---
title: I'm getting a compile error when I try to deserialize JSON with Jackson into polymorphic types using the complete example
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The code example is not valid JSON, so it cannot be deserialized with Jackson.
---

**Contents**

[TOC]

## Section 1: Description of Error
The error occurs when attempting to deserialize a JSON string into a polymorphic type using Jackson. The error message reads: "com.fasterxml.jackson.databind.exc.MismatchedInputException: Cannot deserialize instance of `<PolymorphicType>` out of START_OBJECT token".

## Section 2: Possible Causes
This error can occur when the JSON string does not contain the required information to properly deserialize the polymorphic type. This can happen if the JSON string does not contain the correct type field or if the type field does not match the expected type for the polymorphic type.

## Section 3: Solution
The solution is to ensure that the JSON string contains the correct type field and that it matches the expected type for the polymorphic type. The type field should be included in the JSON string and should match the type of the polymorphic type.

## Section 4: Example
For example, if the polymorphic type is a `Person` and the expected type is `PersonType.EMPLOYEE`, the JSON string should contain the following:
```
{
    "type": "EMPLOYEE",
    ...
}
```
