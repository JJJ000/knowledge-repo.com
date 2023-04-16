---
title: Includes items that are not sensitive to capitalization
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, Javascript has a built-in method called `toLowerCase()` which can be used to make a string case insensitive.
---

**Contents**

[TOC]

##### Case Insensitive String Comparison

In JavaScript, strings can be compared in a case-insensitive manner using the `.toLowerCase()` or `.toUpperCase()` methods. For example:

```
let str1 = "Hello";
let str2 = "hello";

str1.toLowerCase() === str2.toLowerCase(); // true
```

##### Case Insensitive Regex

Regular expressions can also be used in a case-insensitive manner using the `i` flag. For example:

```
let str = "Hello World";
let regex = /hello/i;

regex.test(str); // true
```

##### Case Insensitive Object Keys

When working with objects, keys can be compared in a case-insensitive manner using the `.toLowerCase()` or `.toUpperCase()` methods. For example:

```
let obj = {
  key1: "value1",
  KEY2: "value2"
};

obj[key1.toLowerCase()] === obj[KEY2.toUpperCase()]; // true
```

##### Case Insensitive Array Search

When searching for an element in an array, a case-insensitive search can be performed using the `.includes()` method and the `.toLowerCase()` or `.toUpperCase()` methods. For example:

```
let arr = ["Hello", "World"];
let str = "hello";

arr.includes(str.toLowerCase()); // true
```
