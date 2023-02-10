---
title: Loop through a jsonarray in kotlin
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can iterate through a JSONArray in JSON using a for loop.
---

**Contents**

[TOC]

### 1. Create a JSONArray Object

In order to iterate through a JSONArray, we first need to create a JSONArray object. We can do this by passing a string representation of our JSONArray to the `JSONArray` constructor:

```kotlin
val jsonArrayString = "[1, 2, 3, 4, 5]"
val jsonArray = JSONArray(jsonArrayString)
```

### 2. Iterate Through the JSONArray

Once we have a JSONArray object, we can iterate through it using the `for` loop. Inside the loop, we can access the elements of the JSONArray using the `get` method:

```kotlin
for (i in 0 until jsonArray.length()) {
    val element = jsonArray.get(i)
    // Do something with the element
}
```

### 3. Parse the Elements

The elements of the JSONArray are returned as `Any` objects, so we may need to parse them into their appropriate types. For example, if we know that the elements of the JSONArray are integers, we can parse them into `Int`s using the `toInt` method:

```kotlin
for (i in 0 until jsonArray.length()) {
    val element = jsonArray.get(i)
    val intElement = element.toInt()
    // Do something with the intElement
}
```

### 4. Handle Exceptions

When parsing the elements of the JSONArray, we should handle any exceptions that may occur. For example, if the element is not an integer, we should catch the exception and handle it appropriately:

```kotlin
for (i in 0 until jsonArray.length()) {
    val element = jsonArray.get(i)
    try {
        val intElement = element.toInt()
        // Do something with the intElement
    } catch (e: Exception) {
        // Handle the exception
    }
}
```
