---
title: What is the process for transforming a string into a jsonobject using the gson library?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the Gson.fromJson() method to convert a String to a JsonObject.
---

**Contents**

[TOC]

##1. Add Dependency

Add the Gson dependency to your project.

##2. Create Gson Object

Create a Gson object to parse the string:

```java
Gson gson = new Gson();
```

##3. Parse String

Parse the string to a JsonObject:

```java
JsonObject jsonObject = gson.fromJson(string, JsonObject.class);
```

##4. Use JsonObject

Use the JsonObject to access the data:

```java
String value = jsonObject.get("key").getAsString();
```
