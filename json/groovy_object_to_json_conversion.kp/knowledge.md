---
title: Convert an object to a JSON string using groovy
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: The JsonBuilder class can be used to convert an object to a JSON string.
---

**Contents**

[TOC]

**Section 1: Overview**

JSON (JavaScript Object Notation) is a lightweight data-interchange format that is used for exchanging data between different systems. It is a text-based format that is easy for humans to read and write. In Groovy, the JsonBuilder class provides a convenient way to convert an object to a JSON string.

**Section 2: JsonBuilder Class**

The JsonBuilder class is a utility class for constructing JSON objects. It provides methods for creating JSON objects, arrays, and values. It also provides methods for adding and removing elements from the JSON object.

**Section 3: Converting an Object to a JSON String**

The JsonBuilder class provides the toString() method which can be used to convert an object to a JSON string. This method takes an object as a parameter and returns a JSON string representation of the object.

**Section 4: Example**

For example, the following code snippet creates a JSON string representation of a Person object:

```groovy
def person = new Person(name: 'John', age: 25)
def jsonString = new JsonBuilder(person).toString()
```

The resulting JSON string would look like this:

```json
{
  "name": "John",
  "age": 25
}
```
