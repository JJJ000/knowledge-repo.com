---
title: Comprehending the distinction between object.create() and instantiating a new object with the 'new' keyword
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Object.create() creates an object with the specified prototype object and properties, while new SomeFunction() creates a new object and binds the `this` keyword to the newly created object.
---

**Contents**

[TOC]

### Object.create()
Object.create() is a static method on the Object constructor which creates a new object with the prototype set to a certain object. This method allows you to create an object with the same properties and methods as the provided object.

### new SomeFunction()
new SomeFunction() is a constructor function used to create a new object. The new keyword is used to instantiate a constructor function and create a new object. The newly created object will have access to any methods or properties defined within the constructor function.
