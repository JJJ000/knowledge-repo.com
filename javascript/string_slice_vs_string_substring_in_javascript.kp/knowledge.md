---
title: What distinguishes string.slice from string.substring?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: String.slice allows for negative indices and includes the character at the end index, while String.substring only allows for positive indices and does not include the character at the end index.
---

**Contents**

[TOC]

#### Syntax
String.slice syntax is `string.slice(startIndex[, endIndex])` while String.substring syntax is `string.substring(startIndex[, endIndex])`.

#### Range of Indexes
String.slice allows for negative index values which will be relative to the end of the string, while String.substring does not accept negative index values.

#### Return Value
String.slice returns a new string which contains the characters from the startIndex up to but not including the endIndex. String.substring returns a new string which contains the characters from the startIndex up to but not including the endIndex, but it will stop at the end of the string if the endIndex is greater than the length of the string.

#### Browser Compatibility
String.slice is supported in all major browsers, while String.substring is supported in all browsers except Internet Explorer 8 and below.
