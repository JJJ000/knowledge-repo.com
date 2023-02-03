---
title: Is there a way to determine if a string includes a certain substring?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the String.prototype.includes() method.
---

**Contents**

[TOC]

#### Using the `indexOf()` Method

The `indexOf()` method is used to check if a string contains a substring. If the substring is present, the `indexOf()` method will return the position of the first character of the substring. If the substring is not present, the `indexOf()` method will return -1.

```javascript
let str = "This is a test string";
let subStr = "test";

if (str.indexOf(subStr) !== -1) {
  console.log("The string contains the substring");
} else {
  console.log("The string does not contain the substring");
}
```

#### Using the `includes()` Method

The `includes()` method is used to check if a string contains a substring. It returns a boolean value, `true` if the substring is present and `false` if the substring is not present.

```javascript
let str = "This is a test string";
let subStr = "test";

if (str.includes(subStr)) {
  console.log("The string contains the substring");
} else {
  console.log("The string does not contain the substring");
}
```

#### Using the `search()` Method

The `search()` method is used to check if a string contains a substring. It returns the position of the first character of the substring, if the substring is present and -1 if the substring is not present.

```javascript
let str = "This is a test string";
let subStr = "test";

if (str.search(subStr) !== -1) {
  console.log("The string contains the substring");
} else {
  console.log("The string does not contain the substring");
}
```

#### Using Regular Expressions

Regular expressions can also be used to check if a string contains a substring. The `test()` method of the `RegExp` object returns a boolean value, `true` if the substring is present and `false` if the substring is not present.

```javascript
let str = "This is a test string";
let subStr = "test";

let regex = new RegExp(subStr);

if (regex.test(str)) {
  console.log("The string contains the substring");
} else {
  console.log("The string does not contain the substring");
}
```
