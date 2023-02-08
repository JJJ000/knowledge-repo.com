---
title: Find a substring between two characters using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the String.prototype.substring() method to get the substring between two characters.
---

**Contents**

[TOC]

## Section 1: String Manipulation

In order to get a substring between two characters using JavaScript, you can use the `substring()` method. This method takes two parameters: the start index and the end index of the substring. 

## Section 2: Example

For example, if you have a string `"This is a test string"`, and you want to get the substring between the `"t"` and the `"s"`, you can use the following code:

```javascript
let str = "This is a test string";
let substring = str.substring(str.indexOf("t"), str.indexOf("s"));
console.log(substring); // Output: "his i"
```

## Section 3: Limitations

Note that the `substring()` method does not include the character at the end index, so the output in this example is `"his i"` instead of `"his is"`.

## Section 4: Alternatives

If you need to include the character at the end index, you can use the `substr()` method instead, which takes two parameters: the start index and the length of the substring. The following code will output `"his is"`:

```javascript
let str = "This is a test string";
let substring = str.substr(str.indexOf("t"), str.indexOf("s") - str.indexOf("t") + 1);
console.log(substring); // Output: "his is"
```
