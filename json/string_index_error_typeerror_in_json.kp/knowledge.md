---
title: What does "typeerror string indices must be integers" mean?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The error is caused by attempting to access a string value using an index that is not an integer.
---

**Contents**

[TOC]

# Understanding the Error
The "TypeError: string indices must be integers" error occurs when attempting to access a character in a string using an index that is not an integer. This error is caused by attempting to access a character in a string using a variable or an expression that evaluates to a non-integer value.

# Json
Json is a lightweight data-interchange format. It is used for exchanging data between different systems. The syntax for Json objects is based on the syntax for Javascript objects. This means that when accessing the values of a Json object, the same rules apply as when accessing the values of a Javascript object. This includes the rule that string indices must be integers.

# Example
For example, let's say we have the following Json object:

```
{
  "name": "John",
  "age": 30
}
```

If we attempt to access the value of the "name" key using a non-integer index, we will get the "TypeError: string indices must be integers" error:

```
name = jsonObject["name"] # This will work
name = jsonObject["na" + "me"] # This will cause the error
```

# Solution
The solution to this error is to make sure that the index being used to access the value of a Json object is an integer. If the index is a variable or an expression, make sure that it evaluates to an integer before attempting to access the value.
