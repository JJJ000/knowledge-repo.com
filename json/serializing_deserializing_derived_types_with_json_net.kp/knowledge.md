---
title: How does json.net handle the serialization and deserialization of derived types?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Yes, Json.NET can serialize and deserialize derived types.
---

**Contents**

[TOC]

#### Serialization

Json.net is capable of serializing derived types. When serializing a derived type, Json.net will serialize all of the properties of the base type and all of the properties of the derived type. This allows for the serialization of complex objects with multiple levels of inheritance.

#### Deserialization

Json.net is also capable of deserializing derived types. When deserializing a derived type, Json.net will create an instance of the derived type and populate it with the values of the base type and the derived type. This allows for the deserialization of complex objects with multiple levels of inheritance.

#### Custom Serialization

Json.net also provides the ability to customize the serialization and deserialization of derived types. This allows developers to control the serialization and deserialization of complex objects with multiple levels of inheritance.

#### Custom Deserialization

Json.net also provides the ability to customize the deserialization of derived types. This allows developers to control the deserialization of complex objects with multiple levels of inheritance.
