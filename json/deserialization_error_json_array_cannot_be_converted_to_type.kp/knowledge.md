---
title: The given JSON array (e.g. [1,2,3]) cannot be converted into the specified type through deserialization
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: The JSON array cannot be converted to the specified data type.
---

**Contents**

[TOC]

Section 1: Introduction

When working with JSON in .NET, we may come across a situation where we need to deserialize an array of JSON objects into an object of a specific type. However, sometimes we encounter an error called "Cannot deserialize the current JSON array (e.g. [1,2,3]) into type" which means that the JSON array cannot be mapped to the object type we want to deserialize it into. In this article, we will explore some common reasons why this error occurs and how to fix it.

Section 2: Common Reasons for the Error

There could be several reasons why this error occurs. Some of the most common ones are:

1. The JSON array contains objects that do not match the properties of the target type. For example, the JSON array may contain an extra property or be missing a required property that the target type expects.

2. The JSON array is not structured properly. For example, it may have an extra comma at the end or be missing a closing bracket.

3. The target type is not serializable. Not all types can be serialized and deserialized using JSON. Make sure that the target type has a default constructor and all of its properties have public getters and setters.

Section 3: Fixing the Error

To fix this error, we need to make sure that the JSON array is compatible with the target type we want to deserialize it into. Here are some steps we can take:

1. Check that the JSON array has the expected structure. Make sure that it starts with a "[" and ends with a "]" and that each object inside the array is separated by a ",".

2. Verify that the target type has the same properties as the JSON objects in the array. If the JSON objects in the array have an extra property that the target type does not have, either remove the property from the JSON or add the property to the target type.

3. Make sure that the target type is serializable. If the target type is not serializable, we can create a new class that has the same properties as the target type and is serializable.

Section 4: Conclusion

In this article, we explored the "Cannot deserialize the current JSON array into" error in .NET and identified some common reasons why it occurs. We also discussed some steps we can take to fix the error by ensuring that the JSON array is compatible with the target type we want to deserialize it into. By following these steps, we can deserialize the JSON array successfully without encountering this error.
