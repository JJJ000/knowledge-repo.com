---
title: Regex to substitute multiple spaces with one space
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The regex to replace multiple spaces with a single space in Javascript is /\s+/g.
---

**Contents**

[TOC]

# Section 1: Regex

\s+

# Section 2: Replace Syntax

str.replace(/\s+/g, ' ')

# Section 3: Explanation

The regex \s+ matches one or more whitespace characters, including spaces, tabs, and newlines. The replace syntax replaces all matches of the regex with a single space character.

# Section 4: Example

For example, the following code snippet will replace multiple spaces with a single space:

const str = 'This   is   a   test   string';
const newStr = str.replace(/\s+/g, ' ');
console.log(newStr); // Output: "This is a test string"
