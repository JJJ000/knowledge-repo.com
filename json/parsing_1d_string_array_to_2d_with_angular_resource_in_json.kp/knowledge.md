---
title: Angular resource transforming a single-dimensional array of strings into a two-dimensional array
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Angular Resource can parse a one-dimensional array of strings into a two-dimensional array of objects by using the `transformResponse` option.
---

**Contents**

[TOC]

**Section 1: Create the Array**

To create an array of strings, you can use the `var` keyword to declare a variable and assign an array of strings to it.

```javascript
var stringArray = ["string1", "string2", "string3"];
```

**Section 2: Parse to JSON**

To parse the array of strings to a 2D array in JSON, you can use the `angular.toJson` method. This method takes the array of strings and returns a JSON object.

```javascript
var jsonObject = angular.toJson(stringArray);
```

**Section 3: Parse to 2D Array**

To parse the JSON object to a 2D array, you can use the `angular.fromJson` method. This method takes the JSON object and returns a 2D array.

```javascript
var twoDArray = angular.fromJson(jsonObject);
```

**Section 4: Output 2D Array**

To output the 2D array, you can use the `console.log` method. This method takes the 2D array and prints it to the console.

```javascript
console.log(twoDArray);
```
