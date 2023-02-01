---
title: What are the distinctions between re.search and re.match?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: re.search searches for a pattern anywhere in the string, while re.match only searches for a pattern at the beginning of the string.
---

**Contents**

[TOC]

#### re.search

`re.search` searches for a pattern in a string and returns a match object if the pattern is found. It searches the entire string, even if the pattern is not found at the beginning.

#### re.match

`re.match` only matches the pattern at the beginning of the string and returns a match object if the pattern is found. It does not search the entire string, so the pattern must be found at the beginning of the string for a match object to be returned.
