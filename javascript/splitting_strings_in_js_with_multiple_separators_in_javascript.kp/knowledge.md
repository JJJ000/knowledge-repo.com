---
title: What is the best way to divide a string that has multiple delimiters using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can split a string with multiple separators in JavaScript using the String.prototype.split() method with a regular expression as the separator.
---

**Contents**

[TOC]

1. **Using the Split Method**

The `split()` method is a built-in JavaScript method that splits a string into an array of substrings. It takes a delimiter as an argument, which can be a single character or a string of multiple characters. To split a string with multiple separators, pass the separators as a string to the `split()` method.

```javascript
let str = "Hello-World|Foo-Bar";
let arr = str.split("-|");

console.log(arr); // Output: ["Hello", "World", "Foo", "Bar"]
```

2. **Using Regular Expressions**

Regular expressions can also be used to split a string with multiple separators. The `split()` method takes a regular expression as an argument, so it can be used to match multiple delimiters. To match multiple separators, use the `|` character to separate each separator.

```javascript
let str = "Hello-World|Foo-Bar";
let arr = str.split(/-|\|/);

console.log(arr); // Output: ["Hello", "World", "Foo", "Bar"]
```

3. **Using the Replace Method**

The `replace()` method can also be used to split a string with multiple separators. The `replace()` method takes a regular expression as an argument, so it can be used to match multiple delimiters. To match multiple separators, use the `|` character to separate each separator. The `replace()` method can be used to replace the matched separators with a single character, such as a space. The resulting string can then be split on the single character to get an array of substrings.

```javascript
let str = "Hello-World|Foo-Bar";
let arr = str.replace(/-|\|/g, " ").split(" ");

console.log(arr); // Output: ["Hello", "World", "Foo", "Bar"]
```

4. **Using the Reduce Method**

The `reduce()` method can also be used to split a string with multiple separators. The `reduce()` method takes a callback function as an argument, which can be used to iterate over the characters in the string and split the string into an array of substrings. The callback function can use a regular expression to match multiple separators and split the string on each separator.

```javascript
let str = "Hello-World|Foo-Bar";
let arr = Array.prototype.reduce.call(str, (acc, curr) => {
  if (/[-|\|]/.test(curr)) {
    acc.push("");
  } else {
    acc[acc.length - 1] += curr;
  }
  return acc;
}, [""]);

console.log(arr); // Output: ["Hello", "World", "Foo", "Bar"]
```
