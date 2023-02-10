---
title: Specify the sequence in which the properties of an object should be serialized using Jackson objectmapper
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: It is not possible to specify the serialization order of object properties in JSON using Jackson ObjectMapper.
---

**Contents**

[TOC]

1. Using @JsonPropertyOrder Annotation
The @JsonPropertyOrder annotation can be used to specify the serialization order of object properties in Json.

2. Using @JsonProperty Annotation
The @JsonProperty annotation can be used to specify the order of properties in the serialized Json.

3. Using Jackson Configuration
The Jackson configuration can be used to specify the serialization order of object properties in Json.

4. Using Custom Serializer
A custom serializer can be written to specify the serialization order of object properties in Json.
