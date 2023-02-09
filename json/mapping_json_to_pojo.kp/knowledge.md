---
title: Transform a jsonnode into a plain old Java object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use an ObjectMapper to map the JsonNode to a POJO.
---

**Contents**

[TOC]

### Section 1: Overview

JsonNode is a type of data structure that is used to store JSON data in Java. It can be used to parse, modify, and create JSON data. In order to convert a JsonNode into a POJO (Plain Old Java Object), we need to use an object mapper. An object mapper is a library that allows us to map JSON data to Java objects.

### Section 2: Using an Object Mapper

There are several object mappers available for Java, such as Jackson, Gson, and JSON-B. Each one has its own advantages and disadvantages. For example, Jackson is the most widely used and has the most features, while Gson is simpler and easier to use.

Once you have chosen an object mapper, you can use its API to map the JsonNode to a POJO. The API will take the JsonNode and convert it into an instance of the POJO.

### Section 3: Example

Let's look at an example using Jackson. First, we need to create a POJO to map the JsonNode to. Let's say we have a Person class with three fields: name, age, and address.

```java
public class Person {
    private String name;
    private int age;
    private String address;
    
    // getters and setters
}
```

Next, we need to create an instance of the ObjectMapper.

```java
ObjectMapper mapper = new ObjectMapper();
```

Finally, we can use the mapper to map the JsonNode to the Person object.

```java
Person person = mapper.readValue(jsonNode, Person.class);
```

### Section 4: Conclusion

In conclusion, it is possible to convert a JsonNode into a POJO by using an object mapper. There are several object mappers available for Java, and each one has its own advantages and disadvantages. Once you have chosen an object mapper, you can use its API to map the JsonNode to a POJO.
