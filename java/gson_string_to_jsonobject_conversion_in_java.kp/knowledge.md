---
title: Using gson, convert a string directly into a jsonobject without the need for a plain old Java object (pojo)
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Gson can be used to directly convert a String to a JsonObject in Java without using a POJO.
---

**Contents**

[TOC]

`**` Using Gson Library**

Using Gson Library, we can directly convert a String to a JsonObject without using any POJO. To do this, we will first need to create a Gson object, and then use its fromJson() method with the String as an argument. The fromJson() method will return a JsonObject.

Example:

```java
Gson gson = new Gson();
String jsonString = "{\"name\":\"John\",\"age\":30}";
JsonObject jsonObject = gson.fromJson(jsonString, JsonObject.class);
```

`**` Using JSONObject Library**

Using the JSONObject library, we can also directly convert a String to a JsonObject without using any POJO. To do this, we will first need to create a JSONObject object, and then use its parse() method with the String as an argument. The parse() method will return a JsonObject.

Example:

```java
String jsonString = "{\"name\":\"John\",\"age\":30}";
JSONObject jsonObject = new JSONObject(jsonString);
```

`**` Using Jackson Library**

Using Jackson Library, we can also directly convert a String to a JsonObject without using any POJO. To do this, we will first need to create an ObjectMapper object, and then use its readValue() method with the String as an argument. The readValue() method will return a JsonNode, which can be cast to a JsonObject.

Example:

```java
ObjectMapper mapper = new ObjectMapper();
String jsonString = "{\"name\":\"John\",\"age\":30}";
JsonNode jsonNode = mapper.readValue(jsonString, JsonNode.class);
JsonObject jsonObject = (JsonObject) jsonNode;
```

`**` Using JsonParser Library**

Using the JsonParser library, we can also directly convert a String to a JsonObject without using any POJO. To do this, we will first need to create a JsonParser object, and then use its parse() method with the String as an argument. The parse() method will return a JsonObject.

Example:

```java
JsonParser parser = new JsonParser();
String jsonString = "{\"name\":\"John\",\"age\":30}";
JsonObject jsonObject = parser.parse(jsonString).getAsJsonObject();
```
