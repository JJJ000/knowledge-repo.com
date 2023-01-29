---
title: Using @jsonignore only during the process of serialization, not deserialization
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: @JsonIgnore can be used to prevent fields from being serialized, but it will not prevent them from being deserialized.
---

**Contents**

[TOC]

### Using @JsonIgnore for Serialization

When using the @JsonIgnore annotation on a field in a Java class, it will be ignored during serialization. This means that when an object of the class is serialized, the field annotated with @JsonIgnore will not be included in the JSON output.

### Not Using @JsonIgnore for Deserialization

When using the @JsonIgnore annotation on a field in a Java class, it will not be used during deserialization. This means that when a JSON object is deserialized into an object of the class, the field annotated with @JsonIgnore will not be set. The field will remain null or with the default value.

### Benefits of Not Using @JsonIgnore for Deserialization

Not using @JsonIgnore for deserialization can be beneficial in cases where the field is optional and can be left with a default value. This can help reduce the amount of code needed to handle deserialization.

### Drawbacks of Not Using @JsonIgnore for Deserialization

Not using @JsonIgnore for deserialization can be a drawback in cases where the field is required and must be set with a value. This can lead to unexpected behavior if the field is left with a null or default value.
