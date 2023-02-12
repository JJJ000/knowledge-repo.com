---
title: Ignore properties that are not present when Jackson is used to deserialize JSON into Java objects
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Jackson can be configured to ignore missing properties during deserialization by setting the FAIL\_ON\_UNKNOWN\_PROPERTIES property to false.
---

**Contents**

[TOC]

## Option 1: @JsonIgnoreProperties

The simplest way to ignore missing properties during Jackson JSON deserialization is to use the @JsonIgnoreProperties annotation. This annotation can be applied to a class and it will ignore any properties that are not mapped to fields in the class.

## Option 2: @JsonIgnore

The @JsonIgnore annotation can be used to ignore specific properties during deserialization. This annotation can be applied to a field and it will ignore any properties that are not mapped to that field.

## Option 3: Custom Deserializers

It is also possible to create custom deserializers that can be used to ignore specific properties during deserialization. This approach is more complex than the other two options, but it allows for more fine-grained control over which properties are ignored and how they are handled.

## Option 4: ObjectMapper

Finally, it is possible to configure the ObjectMapper used for deserialization to ignore properties that are not mapped to fields. This can be done by setting the FAIL_ON_UNKNOWN_PROPERTIES property to false. This approach is similar to the @JsonIgnoreProperties annotation, but it allows for more control over the deserialization process.
