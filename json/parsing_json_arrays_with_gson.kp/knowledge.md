---
title: Parsing a JSON array with gson
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: GSON can be used to parse a JSON array by using the fromJson() method.
---

**Contents**

[TOC]

### Section 1: What is GSON?
GSON is a Java library that can be used to convert Java Objects into their JSON representation. It can also be used to convert a JSON string to an equivalent Java object. GSON can work with arbitrary Java objects including pre-existing objects that you do not have source-code of.

### Section 2: How to Use GSON
Using GSON is quite simple. All you need to do is create a Gson instance and then call the toJson() or fromJson() methods. The toJson() method will convert a Java object to its JSON representation, while the fromJson() method will convert a JSON string to an equivalent Java object.

### Section 3: Parsing a JSON Array
When parsing a JSON array using GSON, you will need to create a Java array or a Java collection such as a List or a Set. You can then use the fromJson() method to parse the array and store the resulting objects in the array or collection.

### Section 4: Example
For example, consider the following JSON array:

```json
[
    {
        "name": "John",
        "age": 30
    },
    {
        "name": "Jane",
        "age": 25
    }
]
```

You can parse this array using GSON as follows:

```java
Gson gson = new Gson();

// Create a Java array
Person[] people = gson.fromJson(jsonString, Person[].class);

// Create a Java collection
List<Person> peopleList = gson.fromJson(jsonString, List.class);
```
