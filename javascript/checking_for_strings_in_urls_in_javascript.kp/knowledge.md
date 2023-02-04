---
title: What is the process for determining if a certain string is present in a url?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the String.prototype.includes() method to check if the URL contains a given string.
---

**Contents**

[TOC]

## Using Includes

The `includes()` method can be used to check if a given string is contained within a URL string.

```javascript
let url = "https://www.google.com/";
let str = "google";

if (url.includes(str)) {
  console.log("URL contains the given string");
} else {
  console.log("URL does not contain the given string");
}
```

## Using Search

The `search()` method can be used to check if a given string is contained within a URL string.

```javascript
let url = "https://www.google.com/";
let str = "google";

if (url.search(str) > -1) {
  console.log("URL contains the given string");
} else {
  console.log("URL does not contain the given string");
}
```

## Using IndexOf

The `indexOf()` method can be used to check if a given string is contained within a URL string.

```javascript
let url = "https://www.google.com/";
let str = "google";

if (url.indexOf(str) > -1) {
  console.log("URL contains the given string");
} else {
  console.log("URL does not contain the given string");
}
```

## Using Regular Expression

The `test()` method of a regular expression can be used to check if a given string is contained within a URL string.

```javascript
let url = "https://www.google.com/";
let str = "google";
let regex = new RegExp(str);

if (regex.test(url)) {
  console.log("URL contains the given string");
} else {
  console.log("URL does not contain the given string");
}
```
