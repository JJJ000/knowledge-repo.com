---
title: Change a boolean value into an integer
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Boolean values can be converted to numbers using the Number() function.
---

**Contents**

[TOC]

### Using the Logical OR Operator

The logical OR operator (`||`) can be used to convert a boolean result into a number/integer. The OR operator returns the first truthy value, or the last operand if none of the values are truthy.

For example, if we want to convert `true` to `1`, we can use the OR operator as follows:

```javascript
let booleanResult = true;
let numberResult = booleanResult || 0; // numberResult will be 1
```

Similarly, if we want to convert `false` to `0`, we can use the OR operator as follows:

```javascript
let booleanResult = false;
let numberResult = booleanResult || 0; // numberResult will be 0
```

### Using the Ternary Operator

The ternary operator (`?`) can also be used to convert a boolean result into a number/integer. The ternary operator takes three operands: a condition, a truthy result, and a falsey result.

For example, if we want to convert `true` to `1`, we can use the ternary operator as follows:

```javascript
let booleanResult = true;
let numberResult = booleanResult ? 1 : 0; // numberResult will be 1
```

Similarly, if we want to convert `false` to `0`, we can use the ternary operator as follows:

```javascript
let booleanResult = false;
let numberResult = booleanResult ? 1 : 0; // numberResult will be 0
```

### Using the Bitwise NOT Operator

The bitwise NOT operator (`~`) can also be used to convert a boolean result into a number/integer. The NOT operator will convert a truthy value to `-1` and a falsey value to `0`.

For example, if we want to convert `true` to `1`, we can use the NOT operator as follows:

```javascript
let booleanResult = true;
let numberResult = ~booleanResult; // numberResult will be -1
```

Similarly, if we want to convert `false` to `0`, we can use the NOT operator as follows:

```javascript
let booleanResult = false;
let numberResult = ~booleanResult; // numberResult will be 0
```
