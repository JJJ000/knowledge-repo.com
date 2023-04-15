---
title: Performing JSON deserialization in cases where the input data structure alternates between being an array and an object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use a flexible approach to deserialize JSON, checking the data type (array or object) and adjusting the code accordingly.
---

**Contents**

[TOC]

## Introduction

JSON (JavaScript Object Notation) is a lightweight format that is used to exchange data between different programming languages. It is easy to understand and is widely used because of its simplicity. However, sometimes JSON data can be a bit tricky to deserialize when it is a mix of arrays and objects.

In this article, we will discuss how to deserialize JSON that sometimes contains an array and sometimes contains an object.

## Handling JSON with Arrays and Objects

Deserializer is a concept used in computer science that refers to the process of converting serialized data back into its original form. In the case of JSON, we can use a deserializer to convert the JSON string back into an object.

When JSON contains an array, it is straightforward to deserialize it into a list or an array. However, when JSON sometimes has an object and sometimes has an array, we need to handle it differently.

## How to Handle JSON with Objects and Arrays

When dealing with JSON that sometimes has an object and sometimes has an array, we can implement a custom deserializer to handle the data.

One approach is to check if the JSON string contains an array or an object. If it contains an array, we can use a standard deserializer to convert it into a list. If it contains an object, we can create a custom class with the properties we need and map the JSON properties to the class properties.

Another approach is to use a JSON library that allows you to handle JSON with dynamic types. In this case, you can use methods such as `JsonDocument` or `JToken` to access elements of the JSON data using a dynamic approach.

## Conclusion

Deserializing JSON data that sometimes contains an object and sometimes contains an array can be challenging. However, with the right approach and tools, it is possible to deserialize JSON data into your desired format. In this article, we outlined how to handle JSON with objects and arrays by using custom deserializers or JSON libraries with a dynamic approach.
