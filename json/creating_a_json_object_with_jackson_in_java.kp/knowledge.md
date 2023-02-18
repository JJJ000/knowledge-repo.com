---
title: Construct a JSON object using Jackson in java
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Jackson can be used to create a JSON object in Java by using the ObjectMapper class.
---

**Contents**

[TOC]

# Section 1: Adding Dependencies

In order to use Jackson in Java to create a JSON object, you must first add the necessary dependencies to your project. This can be done by adding the following code to your project's `pom.xml` file:

```xml
<dependency>
  <groupId>com.fasterxml.jackson.core</groupId>
  <artifactId>jackson-databind</artifactId>
  <version>2.9.7</version>
</dependency>
```

# Section 2: Creating the Java Object

Once the dependencies have been added, you can create a Java object to represent the JSON object. This can be done by creating a class with fields that correspond to the key-value pairs in the JSON object.

For example, if you wanted to create a JSON object with two fields, `name` and `age`, you would create a Java class with those two fields:

```java
public class Person {
  private String name;
  private int age;
  
  // Getters and setters
}
```

# Section 3: Creating the JSON Object

Once the Java object has been created, you can use Jackson to create the JSON object. This can be done by creating an instance of the `ObjectMapper` class and then using the `writeValueAsString` method to serialize the Java object into a JSON string.

For example, if you had an instance of the `Person` class, you could create the JSON object like this:

```java
ObjectMapper mapper = new ObjectMapper();
String json = mapper.writeValueAsString(person);
```

# Section 4: Output

After running the code from the previous section, the `json` variable will contain the following JSON object:

```json
{
  "name": "John Doe",
  "age": 42
}
```
