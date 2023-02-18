---
title: Retrieve a value from an array using jq
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: Use the array index to select the desired value from the array.
---

**Contents**

[TOC]

**Section 1: Parsing the Json Array**

In order to select a value from a Json array, you first need to parse the array. This can be done using the `JSON.parse()` method. This method takes a Json string and returns a JavaScript object.

**Section 2: Accessing the Value**

Once the Json array has been parsed, you can access the value you want by using the array notation. For example, if you have an array with two elements, `[1, 2]`, you can access the first element by using `array[0]`.

**Section 3: Iterating Through the Array**

If you need to iterate through the array, you can use a `for` loop. This loop will loop through each element of the array, allowing you to access each value.

**Section 4: Using the Value**

Once you have access to the value, you can use it however you need. You can store it in a variable, use it in an expression, or even pass it to a function.
