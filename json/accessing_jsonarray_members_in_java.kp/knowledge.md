---
title: Retrieving elements from a jsonarray using java
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the get() method to access the members of items in a JSONArray with Java.
---

**Contents**

[TOC]

# Section 1: JSONArray
A JSONArray is a type of JSON-formatted data structure used to store and access collections of data. It is similar to an array in Java, but instead of containing objects, it contains JSONObjects.

# Section 2: Accessing JSONArray
JSONArray can be accessed using the get() method. This method takes an index as a parameter and returns the corresponding element from the array.

# Section 3: Accessing Members of Items
To access members of items in a JSONArray, you can use the getJSONObject() method. This method takes an index as a parameter and returns the corresponding JSONObject from the array. Once you have the JSONObject, you can use the get() method to access its members.

# Section 4: Example
For example, if we have a JSONArray called "people", we can access the name of the first person in the array by using the following code:

```
String name = people.getJSONObject(0).get("name");
```
