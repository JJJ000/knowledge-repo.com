---
title: What is the indentation level that pep8's e128 requires for a continuation line?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: PEP8`s E128 is a warning that indicates a continuation line is not indented enough to match the visual indent of the statement.
---

**Contents**

[TOC]

# Overview

PEP8's E128 is a warning issued by a linter when a continuation line is not indented enough to match the visual indent of the previous line. This warning is intended to improve code readability and maintain consistency across codebases.

# When is E128 Issued?

E128 is issued when a continuation line is not indented enough to match the visual indent of the previous line. This can happen when a long line is split into multiple lines and the subsequent lines are not indented enough to match the indent of the first line.

# How to Fix E128

The easiest way to fix E128 is to simply indent the continuation line to match the indent of the previous line. In Python, this means indenting the continuation line by 4 spaces. This will ensure that the code is properly indented and readable.
