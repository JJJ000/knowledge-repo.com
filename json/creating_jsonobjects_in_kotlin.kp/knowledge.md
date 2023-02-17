---
title: What is the syntax for creating a jsonobject from a string in kotlin?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Use the JSONObject(String) constructor to create a JSONObject from a String in Kotlin.
---

**Contents**

[TOC]

## Section 1: Create a JSONObject

In Kotlin, you can create a JSONObject from a String using the `JSONObject(String)` constructor.

## Section 2: Parse the String

The `JSONObject(String)` constructor will parse the String into a JSONObject. It will take the String and convert it into a JSONObject that can be used for further processing.

## Section 3: Use the JSONObject

The parsed JSONObject can then be used to access and manipulate the data contained within it. You can use the JSONObject's methods to get values, set values, and so on.

## Section 4: Example

For example, you can create a JSONObject from a String like this:

```kotlin
val jsonStr = "{\"name\": \"John\", \"age\": 30}"
val jsonObject = JSONObject(jsonStr)
```

This will create a JSONObject that contains the data from the String. You can then use the JSONObject's methods to access and manipulate the data.
