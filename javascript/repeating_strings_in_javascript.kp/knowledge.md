---
title: In javascript, how to repeat a string a certain number of times
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: To repeat a string a number of times in JavaScript, use the String.prototype.repeat() method.
---

**Contents**

[TOC]

# Section 1: Using a For Loop

The following code will repeat a string a number of times using a for loop:

```
function repeatStringNumTimes(str, num) {
  let repeatedString = '';
  for (let i = 0; i < num; i++) {
    repeatedString += str;
  }
  return repeatedString;
}
```

# Section 2: Using the Repeat Method

The following code will repeat a string a number of times using the `.repeat()` method:

```
function repeatStringNumTimes(str, num) {
  if (num < 0) {
    return '';
  }
  return str.repeat(num);
}
```

# Section 3: Using Recursion

The following code will repeat a string a number of times using recursion:

```
function repeatStringNumTimes(str, num) {
  if (num < 0) {
    return '';
  }
  if (num === 1) {
    return str;
  }
  else {
    return str + repeatStringNumTimes(str, num - 1);
  }
}
```

# Section 4: Using the Array.fill() Method

The following code will repeat a string a number of times using the `Array.fill()` method:

```
function repeatStringNumTimes(str, num) {
  if (num < 0) {
    return '';
  }
  return Array(num + 1).join(str);
}
```
