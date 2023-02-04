---
title: What is the process for looping through a JSON structure?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use a for loop to iterate over the JSON object`s keys and access the values.
---

**Contents**

[TOC]

1. Parse the JSON

Before you can iterate over a JSON structure, you must first parse it. This can be done using the `JSON.parse()` method. This method takes a JSON string as an argument and returns a JavaScript object.

2. Iterate Over the Object

Once the JSON is parsed, you can iterate over the object using a `for...in` loop. This loop will loop through the object's properties and allow you to access the values associated with each property.

3. Access the Values

Once the loop is in place, you can access the values associated with each property. This can be done by simply referencing the property name within the loop.

4. Perform Desired Actions

Once you have accessed the values, you can perform any desired actions with them. This could include manipulating the values, logging them to the console, or performing calculations with them.
