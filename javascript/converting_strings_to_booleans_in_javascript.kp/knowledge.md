---
title: What is the best way to turn a string into a boolean value in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Use the Boolean() constructor to convert a string to a boolean in JavaScript.
---

**Contents**

[TOC]

### Using the Boolean Constructor

The Boolean constructor can be used to convert a string to a boolean. It takes one parameter, the string to be converted. If the string is "true" (case-insensitive), the constructor will return `true`. If the string is "false" (again, case-insensitive), the constructor will return `false`. Any other value will return `false`. 

```javascript
let str = "true";
let bool = new Boolean(str);
console.log(bool); // true
```

### Using the Boolean() Function

The Boolean() function can also be used to convert a string to a boolean. It takes one parameter, the string to be converted. If the string is "true" (case-insensitive), the function will return `true`. If the string is "false" (again, case-insensitive), the function will return `false`. Any other value will return `false`. 

```javascript
let str = "true";
let bool = Boolean(str);
console.log(bool); // true
```

### Using the !! Operator

The double-negation operator (!!) can also be used to convert a string to a boolean. It takes one parameter, the string to be converted. If the string is "true" (case-insensitive), the operator will return `true`. If the string is "false" (again, case-insensitive), the operator will return `false`. Any other value will return `false`. 

```javascript
let str = "true";
let bool = !!str;
console.log(bool); // true
```

### Using the == Operator

The double-equals operator (==) can also be used to convert a string to a boolean. It takes one parameter, the string to be converted. If the string is "true" (case-insensitive), the operator will return `true`. If the string is "false" (again, case-insensitive), the operator will return `false`. Any other value will return `false`. 

```javascript
let str = "true";
let bool = (str == true);
console.log(bool); // true
```
