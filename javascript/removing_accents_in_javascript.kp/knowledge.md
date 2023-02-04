---
title: Eliminate accent marks/diacritical marks from a string in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the String.prototype.normalize() method to remove accents/diacritics from a string.
---

**Contents**

[TOC]

### Using Regular Expressions

Using regular expressions, we can create a pattern to match any accented character and replace it with the unaccented version. For example:

```javascript
let str = "Máximo";
str = str.replace(/[\u0300-\u036f]/g, "");
console.log(str); // Outputs "Maximo"
```

### Using a Map

We can also create a map of characters and their unaccented versions and use it to replace any accented character with the unaccented version. For example:

```javascript
let str = "Máximo";
let accentsMap = {
  "á": "a",
  "é": "e",
  "í": "i",
  "ó": "o",
  "ú": "u"
};

str = str.replace(/[\u0300-\u036f]/g, function(char) {
  return accentsMap[char] || char;
});
console.log(str); // Outputs "Maximo"
```

### Using a Library

We can also use a library such as [latinize](https://www.npmjs.com/package/latinize) to remove accents/diacritics from a string. For example:

```javascript
let str = "Máximo";
let unaccentedStr = latinize(str);
console.log(unaccentedStr); // Outputs "Maximo"
```
