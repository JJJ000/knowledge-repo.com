---
title: Can json.net be used to bypass get-only properties without using jsonignore attributes?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: No, there is no way to ignore get-only properties in Json.NET without using JsonIgnore attributes.
---

**Contents**

[TOC]

1. Using a Custom Contract Resolver

By creating a custom contract resolver, you can use the ShouldSerialize method to determine which properties should be ignored when serializing. This can be done without using the JsonIgnore attribute.

2. Using a Custom Converter

You can also create a custom JsonConverter that implements the ShouldSerialize method to determine which properties should be ignored. This can be done without using the JsonIgnore attribute.

3. Using the JsonSerializerSettings

You can also use the JsonSerializerSettings to specify which properties should be ignored when serializing. This can be done without using the JsonIgnore attribute.

4. Using a Custom Serialization Binder

You can also create a custom serialization binder to determine which properties should be ignored when serializing. This can be done without using the JsonIgnore attribute.
