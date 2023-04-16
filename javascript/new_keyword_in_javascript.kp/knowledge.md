---
title: What does the 'new' keyword do in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The `new` keyword in JavaScript is used to create an instance of an object or invoke a constructor function.
---

**Contents**

[TOC]

### Definition

The 'new' keyword in JavaScript is an operator used to create an instance of an object. It is used with a constructor function to create a new object, with the properties defined by that function.

### Syntax

The syntax for using the 'new' keyword is:

```
new ConstructorFunction([arguments])
```

Where `ConstructorFunction` is the constructor function that will be used to create the new object, and `[arguments]` are any arguments that the constructor function requires.

### Example

For example, the following code creates a new instance of the `Person` constructor function, with the `name` and `age` arguments passed in:

```
let person = new Person('John', 25);
```

### Usage

The 'new' keyword is used to create a new instance of an object, which can then be used in the rest of the code. This is often used when creating objects from a constructor function, as it allows for more complex objects to be created with ease.
