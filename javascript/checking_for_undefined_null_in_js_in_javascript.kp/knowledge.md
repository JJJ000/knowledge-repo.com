---
title: What is the best way to determine if a variable is undefined or null in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: To check for an undefined or null variable in JavaScript, use the comparison operator `===` to compare the variable to both `undefined` and `null`.
---

**Contents**

[TOC]

# Using Strict Equality Operator

The strict equality operator (`===`) can be used to check if a variable is undefined or null.

```javascript
if (variable === undefined || variable === null) {
    // variable is undefined or null
}
```

# Using Typeof Operator

The `typeof` operator can also be used to check if a variable is undefined or null.

```javascript
if (typeof variable === 'undefined' || variable === null) {
    // variable is undefined or null
}
```

# Using Undefined Global Variable

The `undefined` global variable can also be used to check if a variable is undefined or null.

```javascript
if (variable === undefined || variable === null) {
    // variable is undefined or null
}
```

# Using Object.prototype.hasOwnProperty

The `Object.prototype.hasOwnProperty` method can also be used to check if a variable is undefined or null.

```javascript
if (!Object.prototype.hasOwnProperty.call(object, variable) || variable === null) {
    // variable is undefined or null
}
```
