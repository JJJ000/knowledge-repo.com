---
title: Use Jackson to transform a map into json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: Jackson can be used to convert a Map to JSON using its writeValueAsString() method.
---

**Contents**

[TOC]

## Section 1: Overview
The Jackson library is a Java-based library used for converting Java objects to and from JSON format. It can be used to convert a Map to a JSON string.

## Section 2: Steps
1. Add the Jackson library to your project.
2. Create an ObjectMapper instance.
3. Create a Map object.
4. Use the ObjectMapper instance to convert the Map object to a JSON string.

## Section 3: Example
```java
// Create an ObjectMapper instance
ObjectMapper mapper = new ObjectMapper();

// Create a Map object
Map<String, Object> map = new HashMap<>();
map.put("key1", "value1");
map.put("key2", "value2");

// Convert the Map object to a JSON string
String json = mapper.writeValueAsString(map);
System.out.println(json);
```

## Section 4: Output
The output of the above code will be a JSON string like this:
```json
{"key1":"value1","key2":"value2"}
```
