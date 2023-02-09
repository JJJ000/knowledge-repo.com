---
title: The system.object type is not available in .net framework 4.6
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: System.Object is a built-in type in .NET 4.6 and does not need to be imported.
---

**Contents**

[TOC]

1. Overview
--------------------
System.Object is a predefined type in .NET 4.6. It is the ultimate base class of all other types and is the root of the type hierarchy. It is an abstract type, meaning that it cannot be instantiated directly.

2. How to Use System.Object
--------------------
System.Object should not be used directly. Instead, it is used as a base class when creating custom classes. All classes implicitly inherit from System.Object, so all classes have access to the methods and properties defined in System.Object.

3. JSON Support
--------------------
JSON does not directly support System.Object. Instead, it supports a variety of data types such as strings, numbers, arrays, and objects. All of these data types can be represented as objects in JSON.
