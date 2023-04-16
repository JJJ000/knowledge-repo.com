---
title: What is the process for retrieving the sections of a string that were matched by a JavaScript regular expression?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The matched groups can be accessed by using the RegExp.exec() method.
---

**Contents**

[TOC]

#### Using Match

The `match()` method can be used to access the matched groups in a JavaScript regular expression. This method searches a string for a match against a regular expression and returns an array containing the results of that search. The array contains the entire matched string as the first element, followed by the results of any capturing groups that were present in the regular expression.

#### Using Exec

The `exec()` method can also be used to access the matched groups in a JavaScript regular expression. This method executes a search for a match in a specified string. It returns an array containing the entire matched string as the first element, followed by any capturing groups that were present in the regular expression.

#### Using String Match

The `String.match()` method can also be used to access the matched groups in a JavaScript regular expression. This method searches a string for a match against a regular expression and returns an array containing the results of that search. The array contains the entire matched string as the first element, followed by the results of any capturing groups that were present in the regular expression.

#### Using String Replace

The `String.replace()` method can also be used to access the matched groups in a JavaScript regular expression. This method searches a string for a match against a regular expression and returns a new string with some or all matches of a pattern replaced by a replacement. The matched groups can be accessed using the `$1`, `$2`, etc. syntax.
