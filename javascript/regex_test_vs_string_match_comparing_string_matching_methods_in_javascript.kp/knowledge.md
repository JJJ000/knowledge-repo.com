---
title: Determining if a string is compatible with a regular expression using regex.test versus string.match
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Regex.test returns a boolean, whereas string.match returns an array of matches.
---

**Contents**

[TOC]

## regex.test
`regex.test` is a method that takes a regular expression and a string as parameters and returns a boolean value indicating whether or not the string matches the given regular expression. It does not return any additional information about the match.

## string.match
`string.match` is a method that takes a regular expression and a string as parameters and returns an array containing information about the match. The array will contain the matched text as the first element, followed by any capturing groups, and then any flags that were used in the regular expression.
