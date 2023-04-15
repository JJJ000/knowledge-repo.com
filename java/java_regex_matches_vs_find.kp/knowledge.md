---
title: What is the distinction between the matches() and find() methods in Java regex?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: matches() checks if the entire input sequence matches the regex pattern, while find() searches for and returns the first occurrence of a subsequence that matches the regex pattern.
---

**Contents**

[TOC]

### matches()
`matches()` is a method of the `java.util.regex.Matcher` class. It attempts to match the entire input sequence against the pattern. If the match succeeds, it returns `true`. Otherwise, it returns `false`.

### find()
`find()` is also a method of the `java.util.regex.Matcher` class. It attempts to find the next subsequence of the input sequence that matches the pattern. If the match succeeds, it returns `true`. Otherwise, it returns `false`.
