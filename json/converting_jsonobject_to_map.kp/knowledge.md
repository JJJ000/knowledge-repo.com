---
title: Change a jsonobject into a map
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: A JSONObject can be converted to a Map by using the toMap() method.
---

**Contents**

[TOC]

## Section 1: Introduction

JSON (JavaScript Object Notation) is a lightweight data-interchange format used for exchanging structured data between different applications. It is often used to convert data from one format to another, such as from a database to a web page. JSONObject is a Java library that provides a set of methods for manipulating JSON data. It can be used to convert JSON data into a Map.

## Section 2: Overview of JSONObject

JSONObject is a Java library that provides a set of methods for manipulating JSON data. It can be used to parse JSON data, create JSON objects, and access values from JSON objects. It also provides methods for converting JSON data to and from other formats, such as XML and CSV.

## Section 3: Converting JSONObject to Map

JSONObject provides the method `toMap()` which can be used to convert a JSONObject to a Map. The `toMap()` method takes a JSONObject as an argument and returns a Map that contains the key/value pairs from the JSONObject. The keys in the Map are the names of the fields in the JSONObject, and the values are the values associated with those fields.

## Section 4: Example

The following example shows how to convert a JSONObject to a Map:

```java
JSONObject jsonObject = new JSONObject();
jsonObject.put("name", "John");
jsonObject.put("age", 25);

Map<String, Object> map = jsonObject.toMap();
```

In this example, the `toMap()` method is used to convert the JSONObject to a Map. The resulting Map contains the key/value pairs `name:John` and `age:25`.
