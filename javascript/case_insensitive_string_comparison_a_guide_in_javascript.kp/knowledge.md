---
title: What is the process for comparing strings without considering case?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: String comparison can be done case-insensitively in Javascript by using the String.prototype.toLowerCase() or String.prototype.toUpperCase() methods.
---

**Contents**

[TOC]

**Section 1: Using .toUpperCase() and .toLowerCase()**

We can use the `.toUpperCase()` and `.toLowerCase()` methods to convert both strings to the same case before comparison. This comparison will be case insensitive.

**Section 2: Example Code**

Here is an example of how to use the `.toUpperCase()` and `.toLowerCase()` methods to compare two strings:

```javascript
let string1 = "Hello World";
let string2 = "hello world";

if (string1.toUpperCase() === string2.toUpperCase()) {
  console.log("The strings are equal.");
} else {
  console.log("The strings are not equal.");
}
```

**Section 3: Limitations**

Note that this method of comparison is limited to Latin characters. If you are dealing with strings that contain characters from other languages, you should use a different approach.

**Section 4: Alternatives**

An alternative approach is to use the `String.prototype.localeCompare()` method. This method allows you to specify a locale, so you can perform a case insensitive comparison with characters from any language.
