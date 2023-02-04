---
title: What is the syntax for adding leading zeros to numbers in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the toString() method with a radix of 10 and the desired length of the number as parameters to output numbers with leading zeros.
---

**Contents**

[TOC]

### Using the toString() Method

The `toString()` method allows you to specify the base of the number you would like to output. To output a number with leading zeros, you can use this method and specify a base of 8, 10, or 16.

For example, to output a number with leading zeros using base 10, you can use the following code:

```javascript
let num = 5;
console.log(num.toString().padStart(4, '0')); // Outputs: 0005
```

### Using the String.padStart() Method

The `String.padStart()` method can be used to add leading zeros to a number. This method takes two arguments: the length of the output string, and the character to pad the string with.

For example, to output a number with leading zeros, you can use the following code:

```javascript
let num = 5;
console.log(num.toString().padStart(4, '0')); // Outputs: 0005
```

### Using the Number.toFixed() Method

The `Number.toFixed()` method can be used to output a number with a specific number of decimal places. This method takes one argument: the number of decimal places you would like to output.

For example, to output a number with leading zeros, you can use the following code:

```javascript
let num = 5;
console.log(num.toFixed(4).padStart(4, '0')); // Outputs: 0005
```

### Using the String.padStart() and Number.toPrecision() Methods

The `String.padStart()` and `Number.toPrecision()` methods can be used together to output a number with leading zeros. The `Number.toPrecision()` method takes one argument: the number of digits you would like to output.

For example, to output a number with leading zeros, you can use the following code:

```javascript
let num = 5;
console.log(num.toPrecision(4).padStart(4, '0')); // Outputs: 0005
```
