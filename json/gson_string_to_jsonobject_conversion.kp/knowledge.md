---
title: Use gson to directly transform a string into a jsonobject without creating a plain old Java object (pojo)
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Yes, Gson can directly convert a String to a JsonObject without the need for a POJO.
---

**Contents**

[TOC]

### Using Gson
Gson is a Java library that can be used to convert Java Objects into their JSON representation. It can also be used to convert a JSON string to an equivalent Java object.

### Converting String to JsonObject
To convert a String to a JsonObject, we can use the fromJson() method of the Gson class. The fromJson() method takes a String as an argument and returns a JsonObject.

Example:
```
String jsonString = "{\"name\":\"John\",\"age\":30}";
Gson gson = new Gson();
JsonObject jsonObject = gson.fromJson(jsonString, JsonObject.class);
```

### Converting JsonObject to String
To convert a JsonObject to a String, we can use the toJson() method of the Gson class. The toJson() method takes a JsonObject as an argument and returns a String.

Example:
```
JsonObject jsonObject = new JsonObject();
jsonObject.addProperty("name", "John");
jsonObject.addProperty("age", 30);
Gson gson = new Gson();
String jsonString = gson.toJson(jsonObject);
```
