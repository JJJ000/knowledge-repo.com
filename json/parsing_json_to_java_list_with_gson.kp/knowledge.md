---
title: Using gson to convert a JSON array into a java.util.list
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Gson can parse a JSON array into a Java List using the fromJson() method.
---

**Contents**

[TOC]

**Section 1: Overview**

Gson is a Java library that can be used to parse JSON into Java objects. It can be used to parse a JSON array into a Java List object. The Gson library provides the fromJson() method which can be used to parse JSON into a List.

**Section 2: Setting Up Gson**

In order to use the Gson library, it must first be added to the project. This can be done by adding the Gson dependency to the project's build.gradle file. Once the Gson library has been added to the project, it can be imported into the class where it will be used. 

**Section 3: Parsing JSON Array**

Once the Gson library has been imported, the fromJson() method can be used to parse the JSON array into a Java List. The fromJson() method takes two parameters: the JSON string and the type of the List. The type of the List is specified using the TypeToken class. This class can be used to specify the type of the List elements. 

**Section 4: Example**

The following example shows how to parse a JSON array into a Java List using Gson. 

```java
// Create the Gson object
Gson gson = new Gson();

// Create the list type
Type listType = new TypeToken<List<String>>(){}.getType();

// Parse the JSON array into a list
List<String> list = gson.fromJson(jsonString, listType);
```
