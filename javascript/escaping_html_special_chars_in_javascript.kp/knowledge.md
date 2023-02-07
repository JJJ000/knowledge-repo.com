---
title: Is it possible to avoid html special characters in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Yes, you can escape HTML special characters in JavaScript using the escape() or encodeURI() functions.
---

**Contents**

[TOC]

**Section 1: What are HTML Special Chars?** 
HTML special chars are characters that have a special meaning when used in HTML. These characters include the less than sign (<), greater than sign (>), ampersand (&), single quote ('), double quote ("), and forward slash (/) among others.

**Section 2: Why Escape HTML Special Chars?**
HTML special chars need to be escaped when used in HTML to prevent them from being interpreted as HTML code. For example, if the less than sign (<) is not escaped, it would be interpreted as the beginning of an HTML tag.

**Section 3: How to Escape HTML Special Chars in JavaScript?**
HTML special chars can be escaped in JavaScript using the `escape()` function. This function converts any special characters into their corresponding HTML entities. For example, the less than sign (<) would be converted to &lt;.

**Section 4: How to Unescape HTML Special Chars in JavaScript?**
HTML special chars can be unescaped in JavaScript using the `unescape()` function. This function converts HTML entities back into their corresponding special characters. For example, &lt; would be converted back to the less than sign (<).
