---
title: Find the number of times a character appears in a string using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the String.prototype.split() method to split the string into an array of characters, then use the Array.prototype.reduce() method to count the occurrences of the desired character.
---

**Contents**

[TOC]

**Solution 1:**

Using a `for` Loop

```javascript
function countChar(str, char) {
  let count = 0;
  for (let i = 0; i < str.length; i++) {
    if (str.charAt(i) == char) count++;
  }
  return count;
}
```

**Solution 2:**

Using `split` and `filter`

```javascript
function countChar(str, char) {
  return str.split('').filter(c => c == char).length;
}
```

**Solution 3:**

Using `reduce`

```javascript
function countChar(str, char) {
  return str.split('').reduce((acc, curr) => curr === char ? acc + 1 : acc, 0);
}
```

**Solution 4:**

Using `match`

```javascript
function countChar(str, char) {
  return (str.match(new RegExp(char, 'g')) || []).length;
}
```
