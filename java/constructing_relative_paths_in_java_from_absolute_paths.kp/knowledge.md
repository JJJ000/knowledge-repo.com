---
title: What is the process for creating a relative path in Java based on two absolute paths (or urls)?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Path.relativize() method to construct a relative path in Java from two absolute paths (or URLs).
---

**Contents**

[TOC]

### Getting the Paths

The first step in constructing a relative path in Java from two absolute paths is to obtain the two paths. Depending on the context, this could be done in a variety of ways. For example, if the two paths are URLs, they could be obtained by parsing a string containing the URLs, or they could be obtained from a query string.

### Constructing the Relative Path

Once the two paths have been obtained, the next step is to construct the relative path. This can be done using the `java.net.URI` class, which provides a method for constructing a relative path between two absolute paths. The `URI.relativize()` method takes two `URI` objects as parameters and returns a `URI` object representing the relative path.

### Converting to a String

Once the relative path has been constructed, it must be converted to a string before it can be used. This can be done using the `URI.toString()` method, which returns a string representation of the `URI` object.

### Using the Relative Path

Once the relative path has been constructed and converted to a string, it can be used in the desired application. For example, it can be used to construct a URL for a web page, or it can be used to construct a file path for a local file.
