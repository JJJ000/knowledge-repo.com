---
title: How to format a localdatetime object in spring boot using JSON and Java 8
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Spring Boot uses the ISO-8601 format by default for serializing and deserializing Java 8 LocalDateTime objects in JSON.
---

**Contents**

[TOC]

## 1. Spring Boot Configuration

In order to configure Spring Boot to serialize Java 8 LocalDateTime objects to JSON, you need to add the following dependency to your pom.xml:

```xml
<dependency>
    <groupId>com.fasterxml.jackson.datatype</groupId>
    <artifactId>jackson-datatype-jsr310</artifactId>
    <version>2.10.4</version>
</dependency>
```

## 2. Model Class

In your model class, you need to annotate the LocalDateTime field with the @JsonFormat annotation. This annotation takes two parameters:

- The first parameter is the format of the date, which in this case is "yyyy-MM-dd'T'HH:mm:ss.SSSZ".
- The second parameter is the time zone, which in this case is "UTC".

```java
public class MyModel {
    @JsonFormat(shape = JsonFormat.Shape.STRING, pattern = "yyyy-MM-dd'T'HH:mm:ss.SSSZ", timezone = "UTC")
    private LocalDateTime dateTime;
    // ...
}
```

## 3. Serialization

When serializing the model to JSON, the LocalDateTime field will be serialized in the following format:

```json
{
  "dateTime": "2020-12-01T12:00:00.000+0000"
}
```

## 4. Deserialization

When deserializing the JSON into the model, the LocalDateTime field will be parsed from the following format:

```json
{
  "dateTime": "2020-12-01T12:00:00.000+0000"
}
```
