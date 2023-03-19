---
title: Accelerate multiple regular expression replacements in Python 3
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Use compiled regular expressions and apply them with the `re.sub()` function.
---

**Contents**

[TOC]

## Identifying the Problem

The problem that needs to be solved is the slow performance of regular expression replacements in Python 3 when it is necessary to perform them on millions of records.

## Possible Solutions

### 1. Compiling Regex Patterns

One way to speed up regex replacements in Python 3 is to compile the regex pattern before performing the replacement. Compiling a regex pattern means that the pattern is turned into a regular expression object, which can be used repeatedly without having to recompile the pattern each time.

### 2. Using search() instead of match()

In situations where only part of the input string needs to be replaced, using the search() method instead of the match() method can improve performance. This is because the search() method only looks for the first occurrence of a pattern, whereas match() looks for a pattern at the beginning of the string.

### 3. Using subn() instead of sub()

The subn() method is similar to the sub() method, but it returns the number of substitutions made in addition to the modified string. This can be useful for keeping track of the number of replacements made and for performance, as it avoids the unnecessary overhead of creating a new string object for each replacement.

### 4. Using multiprocessing

To speed up regex replacements on millions of records, multiprocessing can be used to parallelize the work across multiple CPU cores. This can be done using Python's multiprocessing module, which allows for the creation of multiple processes that can work on different subsets of the data simultaneously.

## Conclusion

By compiling regex patterns, using search() instead of match(), using subn() instead of sub(), and using multiprocessing, it is possible to significantly speed up regex replacements in Python 3. Depending on the specific use case, some or all of these techniques may be applicable.
