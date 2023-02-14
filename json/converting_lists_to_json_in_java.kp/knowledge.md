---
title: What is the process for converting a list to JSON in java?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: Use the Jackson library to convert a List to Json in Java.
---

**Contents**

[TOC]

**Section 1: Install Gson Library**

The Gson library is a Java library used to convert Java objects into their JSON representation. It can also be used to convert a JSON string to an equivalent Java object.

To install Gson, add the following dependency to your project's pom.xml file:

```xml
<dependency>
    <groupId>com.google.code.gson</groupId>
    <artifactId>gson</artifactId>
    <version>2.8.5</version>
</dependency>
```

**Section 2: Create a List**

Create a List of objects that you want to convert to JSON. For example:

```java
List<String> list = new ArrayList<>();
list.add("item1");
list.add("item2");
list.add("item3");
```

**Section 3: Use Gson to Convert List to JSON String**

Create a Gson instance and use the toJson() method to convert the List to a JSON string:

```java
Gson gson = new Gson();
String json = gson.toJson(list);
```

**Section 4: Print the JSON String**

Print the JSON string to the console:

```java
System.out.println(json);
```

The output will be:

```json
["item1","item2","item3"]
```
