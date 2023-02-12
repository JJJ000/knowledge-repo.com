---
title: What is the process for counting items in JSON data?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the built-in JSON.parse() method to parse the JSON data and use the .length property to count the number of items.
---

**Contents**

[TOC]

## Section 1: Accessing JSON Data

JSON data is a collection of key-value pairs that can be accessed using the same methods used to access data in a JavaScript object. The most common way to access JSON data is by using the `JSON.parse()` method. This method takes a string of JSON data and converts it into an object that can be manipulated in JavaScript.

## Section 2: Counting Items

Once the JSON data has been converted into an object, the items can be counted using the `Object.keys()` method. This method takes the object and returns an array of all the keys in the object. The length of the array can then be used to count the number of items in the JSON data.

## Section 3: Iterating Through Data

Another way to count the number of items in the JSON data is to iterate through the data using a `for` loop. This loop can be used to check each key in the object and increment a counter for each item.

## Section 4: Counting Nested Objects

When dealing with nested objects, the same methods can be used to count the number of items. The `Object.keys()` method can be used to access the keys of the nested objects, and the `for` loop can be used to iterate through each nested object and increment a counter for each item.
