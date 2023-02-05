---
title: What is the process for adding a leading 0 to single-digit numbers?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the String.prototype.padStart() method to prepend 0 to single-digit numbers.
---

**Contents**

[TOC]

## Using ternary operator

The ternary operator is a conditional operator in Javascript which can be used to add 0 to single-digit numbers. The syntax for the ternary operator is as follows:

```
condition ? result1 : result2
```

In this case, the condition would be `number < 10`, with `result1` being `"0" + number` and `result2` being `number`. This can be implemented as follows:

```javascript
const formatNumber = (number) => number < 10 ? "0" + number : number;
```

## Using if-else statement

The if-else statement is another conditional statement in Javascript which can be used to add 0 to single-digit numbers. The syntax for the if-else statement is as follows:

```javascript
if (condition) {
  // result1
} else {
  // result2
}
```

In this case, the condition would be `number < 10`, with `result1` being `"0" + number` and `result2` being `number`. This can be implemented as follows:

```javascript
const formatNumber = (number) => {
  if (number < 10) {
    return "0" + number;
  } else {
    return number;
  }
};
```

## Using String.prototype.padStart()

The `String.prototype.padStart()` method is a built-in method in Javascript which can be used to add 0 to single-digit numbers. The syntax for the `String.prototype.padStart()` method is as follows:

```javascript
string.padStart(targetLength [, padString])
```

In this case, the `targetLength` would be `2` and the `padString` would be `"0"`. This can be implemented as follows:

```javascript
const formatNumber = (number) => number.toString().padStart(2, "0");
```
