---
title: Javascript private functions
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Private methods in Javascript are functions that are only accessible within the scope of the object they are defined in.
---

**Contents**

[TOC]

### Definition

Private methods are functions that can only be accessed within the same class or object. They are not accessible from outside the class or object.

### Advantages

Private methods help maintain the integrity of the code by preventing external code from accessing or modifying the internal state of the class or object. This makes the code more secure and easier to maintain.

### Syntax

In JavaScript, private methods are declared using the `Symbol` object. A `Symbol` is a unique and immutable primitive value that can be used as an identifier for object properties. The syntax for declaring a private method is as follows:

```javascript
const myPrivateMethod = Symbol('myPrivateMethod');

class MyClass {
  [myPrivateMethod]() {
    // private method code
  }
}
```

### Usage

Private methods can be used to encapsulate code that should not be accessible from outside the class or object. This helps keep the code organized and secure.
