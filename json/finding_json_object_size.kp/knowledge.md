---
title: Find the size of the JSON object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The size of a JSON object can be determined by the number of its key-value pairs.
---

**Contents**

[TOC]

1. **Check the size of the JSON object**
   The size of a JSON object can be determined by using the `Object.keys()` method. This method will return an array of all the keys in the JSON object. The size of the JSON object can then be calculated by taking the length of the array returned by the `Object.keys()` method.

2. **Check the size of the JSON string**
   The size of a JSON string can be determined by using the `JSON.stringify()` method. This method will return a string representation of the JSON object. The size of the JSON string can then be calculated by taking the length of the string returned by the `JSON.stringify()` method.

3. **Check the size of the individual elements in the JSON object**
   The size of the individual elements in the JSON object can be determined by using the `JSON.parse()` method. This method will return an array of all the elements in the JSON object. The size of each element can then be calculated by taking the length of the array returned by the `JSON.parse()` method.

4. **Check the size of the individual values in the JSON object**
   The size of the individual values in the JSON object can be determined by using the `JSON.stringify()` method. This method will return a string representation of the JSON object. The size of each value can then be calculated by taking the length of the string returned by the `JSON.stringify()` method.
