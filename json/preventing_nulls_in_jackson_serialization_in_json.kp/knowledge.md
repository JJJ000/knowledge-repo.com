---
title: How can Jackson be prevented from serializing null values in a map and null fields in a bean?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Set the `@JsonInclude` annotation to `Include.NON\_NULL` on the Map or bean.
---

**Contents**

[TOC]

1. Using @JsonInclude
--------------------------------
The @JsonInclude annotation can be used to prevent null values from getting serialized. This annotation can be used at the class level, or at the property level.

At the class level, the annotation can be used as follows:

```
@JsonInclude(JsonInclude.Include.NON_NULL)
public class MyClass {
    ...
}
```

At the property level, the annotation can be used as follows:

```
public class MyClass {
    @JsonInclude(JsonInclude.Include.NON_NULL)
    private String myProperty;
    ...
}
```

2. Using ObjectMapper
--------------------------------
The ObjectMapper class can be used to configure the serialization of null values. This can be done by setting the `SerializationFeature.WRITE_NULL_MAP_VALUES` to false.

```
ObjectMapper mapper = new ObjectMapper();
mapper.configure(SerializationFeature.WRITE_NULL_MAP_VALUES, false);
```

3. Using Custom Serializers
--------------------------------
Custom serializers can be used to prevent null fields from getting serialized. This can be done by overriding the `serialize` method and checking for null values.

```
public class MySerializer extends JsonSerializer<MyClass> {
    @Override
    public void serialize(MyClass value, JsonGenerator gen, SerializerProvider serializers) throws IOException {
        if (value.getMyProperty() != null) {
            gen.writeObject(value.getMyProperty());
        }
    }
}
```

4. Using @JsonSerialize
--------------------------------
The @JsonSerialize annotation can be used to customize the serialization of a property. This can be done by using a custom serializer or by using a custom serializer factory.

```
public class MyClass {
    @JsonSerialize(using = MySerializer.class)
    private String myProperty;
    ...
}
```
