---
title: What is the process for defining static constants in es6 classes?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Static constants in ES6 classes can be declared using the static keyword followed by the constant name and value.
---

**Contents**

[TOC]

### Syntax

ES6 classes in Javascript allow for the declaration of static constants using the `static` keyword.

```javascript
class MyClass {
  static MY_CONSTANT = 'constant value';
}
```

### Usage

Static constants can be accessed using the class name.

```javascript
console.log(MyClass.MY_CONSTANT); // 'constant value'
```

### Benefits

Static constants provide a convenient way to access values without having to create a new instance of the class. This can be especially useful when dealing with configuration values or other data that is shared across all instances of a class.

### Caveats

Static constants are not part of the prototype chain and thus cannot be overridden in subclasses. Additionally, they are not enumerable, so they will not show up in `Object.keys()` or `for-in` loops.
