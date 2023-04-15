---
title: What is the process for deserialising an array of objects using Jackson?
authors:
- cool_wizard
tags:
- java
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `ObjectMapper` class to deserialise the array of objects in JSON.
---

**Contents**

[TOC]

### Setup

1. Include the Jackson library in your project.
2. Create a class for the objects you want to deserialize.

### Deserialization

1. Create an instance of the `ObjectMapper` class.
2. Use the `readValue()` method of the `ObjectMapper` class to deserialize a JSON array into an array of your class objects.

### Example

Consider the following JSON array:

```json
[
  {
    "name": "John",
    "age": 25
  },
  {
    "name": "Alice",
    "age": 30
  }
]
```

We can deserialize this array into an array of Person objects:

```java
public class Person {
    private String name;
    private int age;
    // getters and setters
}

ObjectMapper mapper = new ObjectMapper();
Person[] people = mapper.readValue(jsonString, Person[].class);
```
