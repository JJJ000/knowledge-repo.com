---
title: Setting up objectmapper in spring
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Spring can be configured to use an ObjectMapper to serialize and deserialize JSON objects.
---

**Contents**

[TOC]

## Section 1 - Adding ObjectMapper to Spring

ObjectMapper can be added to Spring by including the following dependency in the project's pom.xml file:

```
<dependency>
    <groupId>com.fasterxml.jackson.core</groupId>
    <artifactId>jackson-databind</artifactId>
    <version>2.9.9</version>
</dependency>
```

## Section 2 - Configuring ObjectMapper in Spring

ObjectMapper in Spring can be configured by adding the following lines of code to the application configuration class:

```
@Bean
public ObjectMapper objectMapper() {
    ObjectMapper mapper = new ObjectMapper();
    mapper.configure(DeserializationFeature.FAIL_ON_UNKNOWN_PROPERTIES, false);
    mapper.configure(SerializationFeature.WRITE_DATES_AS_TIMESTAMPS, false);
    mapper.setSerializationInclusion(JsonInclude.Include.NON_NULL);
    return mapper;
}
```

## Section 3 - Using ObjectMapper in Spring

ObjectMapper can be used in Spring by autowiring it in the class where it needs to be used:

```
@Autowired
private ObjectMapper objectMapper;
```

## Section 4 - Examples of Using ObjectMapper

ObjectMapper can be used to serialize and deserialize Java objects to and from JSON. For example, the following code can be used to serialize a Java object to a JSON string:

```
String jsonString = objectMapper.writeValueAsString(myObject);
```

Similarly, the following code can be used to deserialize a JSON string to a Java object:

```
MyObject myObject = objectMapper.readValue(jsonString, MyObject.class);
```
