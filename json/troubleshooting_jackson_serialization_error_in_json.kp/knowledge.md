---
title: What is the cause of not being able to serialize using Jackson (json)?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Ensure that all classes being serialized have a default constructor or are annotated with @JsonCreator.
---

**Contents**

[TOC]

**Section 1: Understanding the Issue**
The "No serializer found" error is a common issue when working with Jackson (JSON) that occurs when Jackson is unable to locate a serializer to use for the given object type. This can happen when an object type is not supported by Jackson, or when the object type is not registered with Jackson.

**Section 2: Troubleshooting the Issue**
The first step in troubleshooting the issue is to ensure that the object type is supported by Jackson. If it is, the next step is to check if the object type is registered with Jackson. If it is not, then it must be registered before Jackson can use it.

**Section 3: Registering an Object Type**
To register an object type with Jackson, you must create a custom serializer for the object type. This custom serializer should implement the JacksonSerializer interface and must be registered with Jackson using the registerModule() method.

**Section 4: Conclusion**
By understanding the issue, troubleshooting the issue, and registering an object type with Jackson, the "No serializer found" error can be resolved. This will allow Jackson to properly serialize the given object type.
