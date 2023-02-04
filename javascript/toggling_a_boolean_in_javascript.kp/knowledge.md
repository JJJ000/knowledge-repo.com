---
title: What is the process for changing a boolean value?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the `!` operator to toggle a boolean in Javascript.
---

**Contents**

[TOC]

# Using the Not Operator

The simplest way to toggle a boolean is to use the logical not operator (`!`). This operator flips the value of a boolean from `true` to `false`, or from `false` to `true`.

```javascript
let booleanValue = true;
booleanValue = !booleanValue; // booleanValue is now false
```

# Using the Ternary Operator

Another way to toggle a boolean is to use the ternary operator. This operator is a shortcut for an `if` statement that evaluates a condition and returns one of two values.

```javascript
let booleanValue = true;
booleanValue = booleanValue ? false : true; // booleanValue is now false
```

# Using an If Statement

The most verbose way to toggle a boolean is to use an `if` statement. This statement evaluates a condition and then executes a block of code based on the result.

```javascript
let booleanValue = true;
if (booleanValue) {
  booleanValue = false;
} else {
  booleanValue = true;
} // booleanValue is now false
```
