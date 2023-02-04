---
title: Determine if a variable is a number or a string in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use the typeof operator to check whether a variable is a number or a string in JavaScript.
---

**Contents**

[TOC]

# Using typeof Operator
The typeof operator is used to get the data type of its operand. It returns a string indicating the type of the unevaluated operand.

For example:

```
let num = 10;
let str = "Hello";

console.log(typeof num); // returns "number"
console.log(typeof str); // returns "string"
```

# Using isNaN() Function
The isNaN() function determines whether a value is an illegal number (Not-a-Number). It returns true if the value is NaN, and false if not.

For example:

```
let num = 10;
let str = "Hello";

console.log(isNaN(num)); // returns false
console.log(isNaN(str)); // returns true
```

# Using parseInt() Function
The parseInt() function parses a string and returns an integer. If the first character in the string can't be converted into a number, it returns NaN.

For example:

```
let num = 10;
let str = "Hello";

console.log(parseInt(num)); // returns 10
console.log(parseInt(str)); // returns NaN
```

# Using instanceof Operator
The instanceof operator is used to check whether an object is an instance of a particular type. It returns true if the object is an instance of the specified type, and false if not.

For example:

```
let num = 10;
let str = "Hello";

console.log(num instanceof Number); // returns true
console.log(str instanceof String); // returns true
```
