---
title: What is the equivalent of JavaScript isset()?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The closest equivalent to PHP`s isset() in JavaScript is the `in` operator.
---

**Contents**

[TOC]

# Using typeof

The `typeof` operator can be used to check if a variable has been declared and assigned a value. 

```javascript
if (typeof variableName !== 'undefined') {
  // variable has been declared and is not undefined
}
```

# Using the 'in' operator

The `in` operator can be used to check if a property exists in an object.

```javascript
if ('propertyName' in objectName) {
  // property exists in object
}
```

# Using the hasOwnProperty() method

The `hasOwnProperty()` method can be used to check if a property exists in an object.

```javascript
if (objectName.hasOwnProperty('propertyName')) {
  // property exists in object
}
```

# Using the try/catch block

The `try/catch` block can be used to check if a variable has been declared and assigned a value.

```javascript
try {
  if (variableName !== undefined) {
    // variable has been declared and is not undefined
  }
} catch (err) {}
```
