---
title: What are the distinctions between getpath(), getabsolutepath(), and getcanonicalpath() when used in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: getPath() returns the path of the file as it was declared, getAbsolutePath() returns the absolute path of the file, and getCanonicalPath() returns the canonical path of the file, which is the absolute path of the file after it has been resolved.
---

**Contents**

[TOC]

### getPath()

The `getPath()` method returns the path of the file as a String. This path is relative to the current working directory.

### getAbsolutePath()

The `getAbsolutePath()` method returns the absolute path of the file as a String. This path is an absolute path and is not relative to the current working directory.

### getCanonicalPath()

The `getCanonicalPath()` method returns the canonical path of the file as a String. This path is also an absolute path and is not relative to the current working directory. However, it will also resolve any symbolic links and return the real path of the file.
