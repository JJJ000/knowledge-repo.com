---
title: What is the best way to determine if a string is empty, undefined, or null in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can check for an empty/undefined/null string in JavaScript by using the comparison operator `===` to compare the string to null, undefined, or an empty string (``).
---

**Contents**

[TOC]

#Option 1: Using the Equality Operator

The simplest way to check for an empty string is to use the equality operator (==). This will check if the two values on either side of the operator are equal in value.

```
var myString = '';
if (myString == '') {
    // String is empty
}
```

#Option 2: Using the Length Property

Another way to check for an empty string is to use the length property. This will check the length of the string and return a value of 0 if the string is empty.

```
var myString = '';
if (myString.length == 0) {
    // String is empty
}
```

#Option 3: Using the Boolean Value

The boolean value of an empty string is false, so you can also use the boolean value to check for an empty string.

```
var myString = '';
if (!myString) {
    // String is empty
}
```

#Option 4: Using Undefined or Null

Finally, you can also check for an empty string by checking if the string is undefined or null.

```
var myString = '';
if (myString === undefined || myString === null) {
    // String is empty
}
```
