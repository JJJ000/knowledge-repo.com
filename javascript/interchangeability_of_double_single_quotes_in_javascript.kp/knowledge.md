---
title: Can single and double quotes be used interchangeably in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: No, double quotes are used for strings and single quotes are used for characters.
---

**Contents**

[TOC]

## No
Double and single quotes are not interchangeable in JavaScript.

## Reason
In JavaScript, double quotes are used to denote strings, while single quotes are used to denote characters. Therefore, double and single quotes cannot be used interchangeably as they have different meanings.

## Examples
For example, the following code snippet will not work as double and single quotes are not interchangeable:

```javascript
let str = 'Hello World';
console.log("str);
```

The correct syntax would be:

```javascript
let str = "Hello World";
console.log(str);
```
