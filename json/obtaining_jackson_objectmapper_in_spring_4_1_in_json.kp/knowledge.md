---
title: What is the process for accessing the Jackson objectmapper with spring 4.1?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can obtain the Jackson ObjectMapper in use by Spring 4.1 by autowiring it into your bean.
---

**Contents**

[TOC]

1. Add Dependency
------------
Add the following dependency to your pom.xml file:

```xml
<dependency>
    <groupId>com.fasterxml.jackson.core</groupId>
    <artifactId>jackson-databind</artifactId>
    <version>2.9.9</version>
</dependency>
```

2. Create ObjectMapper
------------
Create an ObjectMapper object and configure it to use the default Spring 4.1 configuration:

```java
ObjectMapper mapper = new ObjectMapper();
mapper.configure(DeserializationFeature.FAIL_ON_UNKNOWN_PROPERTIES, false);
mapper.configure(SerializationFeature.WRITE_DATES_AS_TIMESTAMPS, false);
```

3. Use ObjectMapper
------------
Use the ObjectMapper to serialize and deserialize JSON:

```java
// Serialize
String json = mapper.writeValueAsString(object);

// Deserialize
MyObject object = mapper.readValue(json, MyObject.class);
```

4. Register ObjectMapper
------------
Register the ObjectMapper with Spring 4.1:

```java
@Bean
public ObjectMapper objectMapper() {
    return mapper;
}
```
