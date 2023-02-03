---
title: What is the best way to access the final characters of a string?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the substr() method to get the last characters of a string in Javascript.
---

**Contents**

[TOC]

## Using Substring

Using the `substring` method, you can get the last characters of a string. The `substring` method takes two parameters: the starting index, and the ending index. To get the last characters of a string, you need to start at the index of the string length minus the number of characters you want to get, and end at the string length.

For example, if you want to get the last 3 characters of the string `"Hello World"`, you would use the following code:

```javascript
var last3Chars = "Hello World".substring("Hello World".length - 3, "Hello World".length);
```

## Using Slice

Using the `slice` method, you can get the last characters of a string. The `slice` method takes two parameters: the starting index, and the ending index (which is optional). To get the last characters of a string, you need to start at the index of the string length minus the number of characters you want to get, and leave the ending index blank.

For example, if you want to get the last 3 characters of the string `"Hello World"`, you would use the following code:

```javascript
var last3Chars = "Hello World".slice("Hello World".length - 3);
```

## Using Substr

Using the `substr` method, you can get the last characters of a string. The `substr` method takes two parameters: the starting index, and the number of characters you want to get. To get the last characters of a string, you need to start at the index of the string length minus the number of characters you want to get, and specify the number of characters you want to get.

For example, if you want to get the last 3 characters of the string `"Hello World"`, you would use the following code:

```javascript
var last3Chars = "Hello World".substr("Hello World".length - 3, 3);
```

## Using Split

Using the `split` method, you can get the last characters of a string. The `split` method takes one parameter: the character you want to split the string on. To get the last characters of a string, you need to split the string on an empty string, and then get the last element from the resulting array.

For example, if you want to get the last 3 characters of the string `"Hello World"`, you would use the following code:

```javascript
var last3Chars = "Hello World".split("").slice(-3).join("");
```
