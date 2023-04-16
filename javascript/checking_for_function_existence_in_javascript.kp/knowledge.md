---
title: What is the process for determining if a function exists in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the typeof operator to check if a function exists in JavaScript.
---

**Contents**

[TOC]

1. Using `typeof` Operator
--------------------------------
The `typeof` operator can be used to check if a function exists in Javascript. It will return `function` if the function exists and `undefined` if it does not.

```javascript
if (typeof myFunction === 'function') {
    // Function exists
} else {
    // Function does not exist
}
```

2. Using `try...catch` Block
--------------------------------
The `try...catch` block can be used to check if a function exists in Javascript. If the function exists, the `try` block will be executed. If it does not exist, the `catch` block will be executed.

```javascript
try {
    myFunction();
    // Function exists
} catch {
    // Function does not exist
}
```

3. Using `in` Operator
--------------------------------
The `in` operator can be used to check if a function exists in Javascript. It will return `true` if the function exists and `false` if it does not.

```javascript
if ('myFunction' in window) {
    // Function exists
} else {
    // Function does not exist
}
```

4. Using `hasOwnProperty()` Method
--------------------------------
The `hasOwnProperty()` method can be used to check if a function exists in Javascript. It will return `true` if the function exists and `false` if it does not.

```javascript
if (window.hasOwnProperty('myFunction')) {
    // Function exists
} else {
    // Function does not exist
}
```
