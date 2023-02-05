---
title: There is a syntaxerror because a non-ascii character (the pound sign '£') has been used in the file, and the function is returning it
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: This is a UnicodeDecodeError, and can be resolved by adding the encoding=`utf-8` argument to the open() function.
---

**Contents**

[TOC]

# Solution

## Introduction

SyntaxError occurs when Python encounters a non-ASCII character in a file. In this case, the non-ASCII character is '£' which is returned by a function. This article will explain how to solve this error.

## Solution

The solution is to add the following line to the top of the file:

`# -*- coding: utf-8 -*-`

This line tells Python that the file contains characters encoded in UTF-8. This will allow Python to correctly interpret the non-ASCII character '£'.

## Testing the Solution

To test the solution, the function should be executed again. If the SyntaxError is no longer present, the solution has been successful.

## Conclusion

This article has explained how to solve the SyntaxError caused by a non-ASCII character '£' returned by a function. The solution is to add the line `# -*- coding: utf-8 -*-` to the top of the file. This will allow Python to correctly interpret the non-ASCII character.
