---
title: What is the best way to instruct Jackson to not include a field in the serialization process if its value is null?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the @JsonInclude annotation with the value JsonInclude.Include.NON\_NULL to tell Jackson to ignore a field during serialization if its value is null.
---

**Contents**

[TOC]

1. Using @JsonInclude
---------------------------------
Using the @JsonInclude annotation, you can tell Jackson to ignore fields with null values during serialization.

To use the annotation, you must first import it:

```java
import com.fasterxml.jackson.annotation.JsonInclude;
```

Then, you can add the annotation to the field you want to ignore if its value is null:

```java
@JsonInclude(JsonInclude.Include.NON_NULL)
private String field;
```

2. Using ObjectMapper
---------------------------------
You can also tell Jackson to ignore fields with null values during serialization using the ObjectMapper class.

To use the ObjectMapper class, you must first import it:

```java
import com.fasterxml.jackson.databind.ObjectMapper;
```

Then, you can create an instance of the ObjectMapper class and call the setSerializationInclusion method, passing in the JsonInclude.Include.NON_NULL enum:

```java
ObjectMapper mapper = new ObjectMapper();
mapper.setSerializationInclusion(JsonInclude.Include.NON_NULL);
```

This will tell Jackson to ignore fields with null values during serialization.
