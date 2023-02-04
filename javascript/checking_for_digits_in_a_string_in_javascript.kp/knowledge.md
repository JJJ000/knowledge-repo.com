---
title: Verify if the string consists of only numbers
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use the regex /^\d+$/ to check if a string contains only digits in Javascript.
---

**Contents**

[TOC]

##### Using Regular Expression

We can use a regular expression to check if a string contains only digits. The expression is as follows:

`/^\d+$/`

This expression checks for a string that contains only numbers.

##### Using isNaN()

The `isNaN()` function can be used to check if a string contains only digits. The following code can be used to check if a string contains only digits:

```
function checkDigits(str) {
  return !isNaN(str);
}
```

##### Using parseInt()

The `parseInt()` function can be used to check if a string contains only digits. The following code can be used to check if a string contains only digits:

```
function checkDigits(str) {
  return parseInt(str) == str;
}
```

##### Using Character Codes

We can also use character codes to check if a string contains only digits. The following code can be used to check if a string contains only digits:

```
function checkDigits(str) {
  for (var i = 0; i < str.length; i++) {
    if (str.charCodeAt(i) < 48 || str.charCodeAt(i) > 57) {
      return false;
    }
  }
  return true;
}
```
