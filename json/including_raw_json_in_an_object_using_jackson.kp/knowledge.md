---
title: What is the process for incorporating raw JSON into an object using jackson?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can include raw JSON in an object using Jackson by using the @JsonRawValue annotation.
---

**Contents**

[TOC]

### 1. Using the @JsonRawValue Annotation
The `@JsonRawValue` annotation can be used to include raw JSON in an object. This annotation is used to indicate that the value of the annotated property should be serialized as is, without any additional serialization.

### 2. Example
The following example shows how to include raw JSON in an object using the `@JsonRawValue` annotation:

```java
public class MyObject {
    @JsonRawValue
    private String rawJson;
    
    // Getters and setters
}
```

### 3. Serializing
When the object is serialized, the raw JSON string will be included in the output without any additional serialization.

### 4. Deserializing
When the object is deserialized, the raw JSON string will be set as is, without any additional deserialization.
