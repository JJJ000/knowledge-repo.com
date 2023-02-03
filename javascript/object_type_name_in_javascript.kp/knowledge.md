---
title: Find out the type of an object
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The type of an object in Javascript can be determined using the typeof operator.
---

**Contents**

[TOC]

#1 Using the typeof Operator

The typeof operator is used to get the datatype of a given variable. It returns a string indicating the type of the unevaluated operand.

Syntax:

typeof operand

Examples:

```
var num = 3;
typeof num; // returns "number"

var str = "Hello World";
typeof str; // returns "string"
```

#2 Using the constructor Property

The constructor property returns the constructor function for all JavaScript variables.

Syntax:

variable.constructor

Examples:

```
var num = 3;
num.constructor; // returns function Number() { [native code] }

var str = "Hello World";
str.constructor; // returns function String() { [native code] }
```

#3 Using the Object.prototype.toString() Method

The Object.prototype.toString() method returns a string representing the object.

Syntax:

Object.prototype.toString.call(variable)

Examples:

```
var num = 3;
Object.prototype.toString.call(num); // returns "[object Number]"

var str = "Hello World";
Object.prototype.toString.call(str); // returns "[object String]"
```

#4 Using the instanceof Operator

The instanceof operator is used to test whether an object has in its prototype chain the prototype property of a constructor.

Syntax:

variable instanceof constructor

Examples:

```
var num = 3;
num instanceof Number; // returns true

var str = "Hello World";
str instanceof String; // returns true
```
