---
title: Jackson how to stop field serialization
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: Use the @JsonIgnore annotation on fields that should not be serialized.
---

**Contents**

[TOC]

1. Using the `@JsonIgnore` Annotation
-------------------------------------
The `@JsonIgnore` annotation can be used to prevent a field from being serialized into JSON. This annotation can be applied to either a field or a getter method.

2. Using the `@JsonIgnoreProperties` Annotation
------------------------------------------------
The `@JsonIgnoreProperties` annotation can be used to ignore multiple fields during serialization. This annotation can be applied to a class.

3. Using the `@JsonProperty` Annotation
---------------------------------------
The `@JsonProperty` annotation can be used to specify the name of the field that will be used during serialization. This annotation can be applied to either a field or a getter method.

4. Using the `@JsonFilter` Annotation
-------------------------------------
The `@JsonFilter` annotation can be used to filter out a specific field during serialization. This annotation can be applied to either a field or a getter method.
