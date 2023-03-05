---
title: Are you interested in concealing certain fields of an object that are being rendered to JSON by jackson?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Add the @JsonIgnore annotation to the fields you want to hide from the JSON output.
---

**Contents**

[TOC]

## Introduction

Jackson is a popular Java library used for converting Java objects to JSON and vice versa. It comes with powerful features and customization options for JSON serialization and deserialization. However, sometimes, we need to hide some fields of an object that are being mapped to JSON by Jackson. In this article, we will explore some approaches to achieve this.

## Using Jackson's `@JsonIgnore` Annotation

Jackson provides an `@JsonIgnore` annotation that can be used to ignore a particular field during the JSON serialization process. This annotation can be applied on the getter method or field itself. When the annotation is applied on the field, it will be ignored by both the serialization and deserialization process. Here's an example:

```java
public class User {
    private Long id;
    private String name;

    @JsonIgnore
    private String password;

    // getters and setters
}
```

In this example, the `password` field will be ignored during JSON serialization.

## Using Jackson's `@JsonView` Annotation

Jackson also provides a `@JsonView` annotation that can be used to specify a view that defines which fields should be included or excluded during JSON serialization. A view is a marker interface that groups fields based on their visibility. Here's an example:

```java
public interface PublicView {}

public interface PrivateView extends PublicView {}

public class User {
    @JsonView(PublicView.class)
    private Long id;

    @JsonView(PublicView.class)
    private String name;

    @JsonView(PrivateView.class)
    private String password;

    // getters and setters
}
```

In this example, the `id` and `name` fields will be included in the JSON output for the `PublicView`, while the `password` field will be included for `PrivateView`.

## Using Custom Jackson Serializer

If the above approaches do not fit your requirements, you can create your custom serializer that controls how an object should be serialized to JSON. You can extend the `JsonSerializer` class, and annotate the field with `@JsonSerialize(using = YourSerializerClass.class)`. Here's an example:

```java
public class User {
    private Long id;
    private String name;

    @JsonSerialize(using = PasswordSerializer.class)
    private String password;

    // getters and setters
}

public class PasswordSerializer extends JsonSerializer<String> {
    @Override
    public void serialize(String value, JsonGenerator gen, SerializerProvider serializers) throws IOException {
        // custom logic to serialize password field
    }
}
```

In this example, the `PasswordSerializer` class controls how the `password` field should be serialized to JSON.

## Conclusion

In this article, we explored some approaches that can be used to hide some fields of an object that are being mapped to JSON by Jackson. You can choose any approach that fits your requirements.
