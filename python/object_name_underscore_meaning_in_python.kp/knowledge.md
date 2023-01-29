---
title: What do the single and double underscores in front of an object name signify?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Single underscore before an object name in Python indicates that the object is private, while double underscore before an object name indicates that the object is strongly private.
---

**Contents**

[TOC]

### Single Underscore

A single underscore before an object name in Python indicates that the object is meant to be private. It's a way of hinting to other developers that the object is not part of the public API, and should not be used directly.

### Double Underscore

A double underscore before an object name in Python indicates that the object is meant to be strongly private. It's a way of hinting to other developers that the object is not part of the public API, and should not be used directly. This is sometimes referred to as "name mangling" as it changes the name of the object in order to make it more difficult to access.
