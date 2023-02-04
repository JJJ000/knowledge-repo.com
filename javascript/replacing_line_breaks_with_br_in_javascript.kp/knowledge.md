---
title: What is the best way to replace all line breaks in a string with <br /> elements?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the replace() method to replace all line breaks with <br /> elements.
---

**Contents**

[TOC]

**Using Regular Expressions**

1. Create a regular expression to match all line breaks in the string. 
   ```javascript
   const regex = /\r?\n/g;
   ```
2. Use the `String.prototype.replace()` method to replace all line breaks with the `<br />` element.
   ```javascript
   const replacedString = string.replace(regex, '<br />');
   ```

**Using String.prototype.split() and Array.prototype.join()**

1. Use the `String.prototype.split()` method to split the string into an array of substrings.
   ```javascript
   const substrings = string.split('\n');
   ```
2. Use the `Array.prototype.join()` method to join the substrings in the array, using the `<br />` element as the separator.
   ```javascript
   const replacedString = substrings.join('<br />');
   ```
