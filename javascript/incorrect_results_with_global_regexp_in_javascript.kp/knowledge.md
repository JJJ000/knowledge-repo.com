---
title: What is causing a regexp with the global flag to produce inaccurate results?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The global flag causes the RegExp to continue searching for matches after finding the first one, which can lead to incorrect results.
---

**Contents**

[TOC]

#1 Poorly Formed Regex
A RegExp with the global flag can give incorrect results if the regular expression is not properly formed. For example, an incorrect syntax can lead to unexpected matches.

#2 Overlapping Matches
A RegExp with the global flag can also give incorrect results if the expression contains overlapping matches. For example, if the expression is looking for a pattern that appears multiple times within a string, the global flag may return incorrect matches.

#3 Unintended Results
The global flag can also give unexpected results if the expression is looking for a pattern that appears multiple times in a string but the expression is not looking for the exact pattern. For example, if the expression is looking for a character that appears multiple times in a string but the expression does not specify the exact character, the global flag may return incorrect matches.

#4 Wrong Usage
Incorrect usage of the global flag can also lead to unexpected results. For example, if the expression is expecting a single match but the global flag is used, the expression may return multiple matches.
