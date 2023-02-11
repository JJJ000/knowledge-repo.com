---
title: Convert JSON data into a format that can be read, including both known and unknown fields
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can deserialize a JSON with known and unknown fields by using a library that supports dynamic field mapping.
---

**Contents**

[TOC]

#### Deserializing with Known Fields

When deserializing JSON with known fields, the most common approach is to create a data structure that matches the JSON object, and then use a library such as Jackson or Gson to map the JSON to the data structure.

For example, if the JSON object looks like this:

```json
{
  "name": "John",
  "age": 30
}
```

We can create a data structure that looks like this:

```java
class Person {
  String name;
  int age;
}
```

Then, using Jackson or Gson, we can map the JSON object to the data structure:

```java
Person person = new ObjectMapper().readValue(json, Person.class);
```

#### Deserializing with Unknown Fields

When deserializing JSON with unknown fields, the most common approach is to use a library such as Jackson or Gson to map the JSON to a Map.

For example, if the JSON object looks like this:

```json
{
  "name": "John",
  "age": 30,
  "address": "123 Main St"
}
```

We can use Jackson or Gson to map the JSON to a Map:

```java
Map<String, Object> map = new ObjectMapper().readValue(json, new TypeReference<Map<String, Object>>(){});
```

This will create a Map with the keys "name", "age" and "address", and the corresponding values.

#### Deserializing with Unknown and Known Fields

When deserializing JSON with both known and unknown fields, the most common approach is to use a library such as Jackson or Gson to map the JSON to a Map, and then manually map the known fields to their corresponding data structures.

For example, if the JSON object looks like this:

```json
{
  "name": "John",
  "age": 30,
  "address": "123 Main St",
  "other": "something"
}
```

We can use Jackson or Gson to map the JSON to a Map:

```java
Map<String, Object> map = new ObjectMapper().readValue(json, new TypeReference<Map<String, Object>>(){});
```

This will create a Map with the keys "name", "age", "address" and "other", and the corresponding values.

Then, we can manually map the known fields to their corresponding data structures:

```java
Person person = new Person();
person.name = (String) map.get("name");
person.age = (int) map.get("age");
```
