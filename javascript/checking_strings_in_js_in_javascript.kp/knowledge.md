---
title: Determine if a variable is a string in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the typeof operator to check if a variable is a string in JavaScript.
---

**Contents**

[TOC]

#### Using typeof Operator

The `typeof` operator is used to check the data type of a given variable. The `typeof` operator returns a string indicating the type of the variable.

```
let str = "Hello World";

typeof str; // returns "string"
```

#### Using Object.prototype.toString()

The `Object.prototype.toString()` method is used to get the object class of the given variable. It returns a string representation of the object.

```
let str = "Hello World";

Object.prototype.toString.call(str); // returns "[object String]"
```

#### Using instanceof Operator

The `instanceof` operator is used to check the type of an object at runtime. It returns a boolean value indicating whether or not the given object is an instance of the specified type.

```
let str = "Hello World";

str instanceof String; // returns true
```

#### Using Constructor Property

The `constructor` property is used to get the constructor function of an object. It returns a reference to the constructor function that created the instance object.

```
let str = "Hello World";

str.constructor; // returns String()
```
