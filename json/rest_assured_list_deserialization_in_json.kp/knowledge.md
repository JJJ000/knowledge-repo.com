---
title: Rest assured - deserializing a generic list
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: REST Assured can be used to deserialize a generic list from a JSON string using the fromJson() method.
---

**Contents**

[TOC]

#### Section 1: Overview
REST Assured is an open-source Java library that enables developers to test and validate REST services. It provides support for a wide range of HTTP methods, including GET, POST, PUT, DELETE, and PATCH. It also supports various authentication methods and can be used to test web services written in any language. One of the features of REST Assured is the ability to deserialize generic lists of objects from JSON.

#### Section 2: Deserialization
Deserialization is the process of converting a JSON string into an object or a list of objects. REST Assured provides a number of methods to deserialize generic lists of objects from a JSON string. These methods include:

- `fromJson()`: This method takes a JSON string and returns a generic list of objects.
- `fromJsonList()`: This method takes a JSON string and returns a list of generic objects.
- `fromJsonArray()`: This method takes a JSON string and returns an array of generic objects.

#### Section 3: Example
For example, consider the following JSON string:

```
[
  {
    "name": "John",
    "age": 25
  },
  {
    "name": "Jane",
    "age": 22
  }
]
```

Using the `fromJsonList()` method, we can deserialize this JSON string into a list of generic objects:

```
List<Person> people = RestAssured.fromJsonList(jsonString, Person.class);
```

The `people` list will contain two `Person` objects, one for John and one for Jane.

#### Section 4: Conclusion
REST Assured provides support for deserializing generic lists of objects from JSON strings. This feature is useful for converting JSON strings into objects and lists of objects, which can then be used in the application.
