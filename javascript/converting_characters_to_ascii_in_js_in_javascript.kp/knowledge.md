---
title: Translate a character to its ascii code in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The ASCII code of a character can be obtained in JavaScript by using the charCodeAt() method.
---

**Contents**

[TOC]

### Using String.charCodeAt()

The `String.charCodeAt()` method returns the Unicode of the character at the specified index in a string.

Syntax:

```
str.charCodeAt(index)
```

Example:

```
let str = 'Hello World!';
let charCode = str.charCodeAt(0); // returns 72
```

### Using fromCharCode()

The `String.fromCharCode()` method returns a string created from the specified sequence of Unicode values.

Syntax:

```
String.fromCharCode(num1[, ...[, numN]])
```

Example:

```
let ascii = String.fromCharCode(72); // returns 'H'
```
