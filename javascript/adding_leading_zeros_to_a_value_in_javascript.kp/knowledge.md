---
title: What is the best way to add zeros to the beginning of a value?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can pad a value with leading zeros by using the toString() method with a specified radix, such as toString(2) for binary or toString(8) for octal.
---

**Contents**

[TOC]

### Using String.prototype.padStart()

The `String.prototype.padStart()` method can be used to pad a string with leading zeros. This method takes two arguments: the target length of the string and the padding character.

```javascript
let myString = '123';
let paddedString = myString.padStart(5, '0');
// paddedString = '00123'
```

### Using String.prototype.padEnd()

The `String.prototype.padEnd()` method can also be used to pad a string with leading zeros. This method takes two arguments: the target length of the string and the padding character.

```javascript
let myString = '123';
let paddedString = myString.padEnd(5, '0');
// paddedString = '12300'
```

### Using a For Loop

A for loop can also be used to pad a string with leading zeros. This approach takes the length of the string and appends a zero until the desired length is reached.

```javascript
let myString = '123';
let paddedString = '';

for (let i = 0; i < 5 - myString.length; i++) {
  paddedString += '0';
}

paddedString += myString;
// paddedString = '00123'
```

### Using Template Literals

Template literals can also be used to pad a string with leading zeros. This approach uses a template literal with the `String.prototype.repeat()` method to generate the desired number of leading zeros.

```javascript
let myString = '123';
let paddedString = `${"0".repeat(5 - myString.length)}${myString}`;
// paddedString = '00123'
```
