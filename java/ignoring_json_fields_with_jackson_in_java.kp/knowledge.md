---
title: Handling JSON objects with Jackson while disregarding new fields
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Jackson can be configured to ignore unknown properties by setting its DeserializationFeature to FAIL\_ON\_UNKNOWN\_PROPERTIES to false.
---

**Contents**

[TOC]

### 1. Using @JsonIgnore
Using the @JsonIgnore annotation on the field in question will cause Jackson to ignore it when serializing/deserializing an object.

For example:
```java
class Example {
    @JsonIgnore
    private String someField;
}
```

### 2. Using @JsonIgnoreProperties
Using the @JsonIgnoreProperties annotation on the class in question will cause Jackson to ignore all fields specified in the annotation.

For example:
```java
@JsonIgnoreProperties({"someField"})
class Example {
    private String someField;
}
```

### 3. Using @JsonIgnoreType
Using the @JsonIgnoreType annotation on the class in question will cause Jackson to ignore all fields of the specified type.

For example:
```java
@JsonIgnoreType
class SomeType {
    private String someField;
}

class Example {
    private SomeType someType;
}
```

### 4. Using Custom Serializers/Deserializers
Using custom serializers and deserializers is a more involved approach, but allows for more control over the serialization/deserialization process.

For example:
```java
public class ExampleSerializer extends StdSerializer<Example> {
    public ExampleSerializer() {
        super(Example.class);
    }

    @Override
    public void serialize(Example value, JsonGenerator gen, SerializerProvider provider) throws IOException {
        // Do not include someField in serialization
    }
}
```
