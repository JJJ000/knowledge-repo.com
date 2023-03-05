---
title: Determine whether it is a jsonobject or jsonarray
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: To test if it is a JSONObject or JSONArray in JSON, use the `instanceof` operator in the programming language being used.
---

**Contents**

[TOC]

## Introduction

In JSON (JavaScript Object Notation), data is represented as key-value pairs or an array of values. Sometimes we need to identify whether the data is a JSON Object or a JSON Array. In this tutorial, we will discuss how to check if you have received a JSONObject or JSONArray.

## Steps to Check Whether it's a JSONObject or JSONArray

There are different methods to check the data and identify whether it's a JSON Object or JSON Array:

### 1. Using instanceof operator

The instanceof operator checks if an object is an instance of a particular class. We can use this operator to check if it's a JSONObject or JSONArray.

```java
    if (jsonObject instanceof JSONObject) {
        // It's a JSONObject
    } else if (jsonObject instanceof JSONArray){
        // It's a JSONArray
    }
```
### 2. Using try-catch

Another method to check whether it's a JSONObject or JSONArray is to use a try-catch block to parse the JSON data. If it's a JSONObject, the JSONParser will parse the data without throwing an exception. If it's a JSONArray, it will throw an exception.

```java
    try {
        JSONObject jsonObject = (JSONObject) parser.parse(jsonData);
        // It's a JSONObject  
     } catch (ClassCastException e) {
           JSONArray jsonArray = (JSONArray) parser.parse(jsonData);
           // It's a JSONArray
     } 
```
### 3. Using the JSONTokener class

The JSONTokener class is used to parse the JSON data. We can pass the JSON data to this class and then check if it's a JSONObject or JSONArray.

```java
    JSONTokener jsonTokener = new JSONTokener(jsonData);
    if (jsonTokener.nextValue() instanceof JSONObject) {
        // It's a JSONObject
    } else if (jsonTokener.nextValue() instanceof JSONArray){
        // It's a JSONArray
    }
```

## Conclusion

In this tutorial, we have discussed various methods to check if it's a JSONObject or JSONArray. We can use any of these methods to identify the type of data we have received.
