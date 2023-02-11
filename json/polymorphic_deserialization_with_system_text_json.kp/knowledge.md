---
title: Can system.text.json be used for polymorphic deserialization?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: No, polymorphic deserialization is not possible in System.Text.Json.
---

**Contents**

[TOC]

## Overview
Polymorphic deserialization is the process of deserializing objects of different types from the same input data. System.Text.Json is a library for working with JSON data in .NET. It does not natively support polymorphic deserialization, but it is possible to implement it with some additional work. 

## Implementing Polymorphic Deserialization
Polymorphic deserialization can be implemented in System.Text.Json by creating a custom converter that can detect the type of the object to be deserialized and use the appropriate converter. This can be done by using the `JsonSerializerOptions.Converters` property to register the custom converter.

The custom converter can then use the `JsonElement.GetProperty("type")` method to determine the type of the object to be deserialized. Once the type is determined, the appropriate converter can be used to deserialize the object. 

## Advantages
Using a custom converter to implement polymorphic deserialization in System.Text.Json has several advantages. It allows for the deserialization of objects of different types from the same input data, which is useful for scenarios where the type of the object is not known beforehand. It also allows for the deserialization of objects that have a common base type, which is useful for scenarios where the exact type of the object is not known but the base type is. 

## Disadvantages
The main disadvantage of using a custom converter to implement polymorphic deserialization in System.Text.Json is the additional complexity it adds to the code. It requires extra code to be written, which can be time-consuming and error-prone. Additionally, the custom converter must be updated whenever the structure of the objects to be deserialized changes, which can be tedious.
