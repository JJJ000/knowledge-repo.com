---
title: What is the most efficient way to reverse a string in-place using javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can reverse a string in-place in JavaScript by using the built-in Array.prototype.reverse() method.
---

**Contents**

[TOC]

#Solution 1: Using the Split, Reverse, and Join Methods

1. Split the string into an array of characters: `let strArr = str.split('');`
2. Reverse the order of the characters in the array: `strArr.reverse();`
3. Join the characters back into a string: `str = strArr.join('');`

#Solution 2: Using a For Loop

1. Create a new empty string to store the reversed string: `let reversed = '';`
2. Iterate through the characters of the original string in reverse order: `for (let i = str.length - 1; i >= 0; i--)`
3. Add each character to the new string: `reversed += str[i];`
4. Set the original string equal to the reversed string: `str = reversed;`
