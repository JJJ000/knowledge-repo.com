---
title: What is the process for transforming a JSON string into a list of Java objects?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the Gson library to deserialize the JSON string into a List of Java objects.
---

**Contents**

[TOC]

### Section 1: Understanding JSON

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used to store and exchange data. It is based on a subset of the JavaScript language and is easy for humans to read and write.

### Section 2: Deserializing JSON

Deserializing JSON is the process of converting a JSON string into a List of Java objects. This can be done using various libraries and frameworks, such as Gson, Jackson, and org.json.

### Section 3: Using Gson

Gson is a popular open-source JSON processing library for Java. It can be used to deserialize a JSON string into a List of Java objects. To do this, first create a Gson object and then use the fromJson() method to deserialize the JSON string into a List.

### Section 4: Example

Consider the following JSON string:

`[{"name":"John","age":25},{"name":"Jane","age":30}]`

The following code snippet shows how to deserialize this JSON string into a List of Java objects using Gson:

```
Gson gson = new Gson();
List<Person> people = gson.fromJson(jsonString, new TypeToken<List<Person>>(){}.getType());
```
