---
title: How can I replace multiple consecutive spaces with a single space in a Java string, and remove any leading and trailing spaces?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use String.trim() and String.replaceAll(`\\s+`, ` `) methods.
---

**Contents**

[TOC]

### Using Regular Expressions

The following code snippet can be used to replace 2 or more spaces with single space in string and delete leading and trailing spaces using Regular Expressions:

```
String str = "   This is a   string   with   multiple   spaces   ";
str = str.replaceAll("\\s+", " ").trim();
```

### Using String.replace and String.trim

The following code snippet can be used to replace 2 or more spaces with single space in string and delete leading and trailing spaces using String.replace and String.trim:

```
String str = "   This is a   string   with   multiple   spaces   ";
str = str.replace("  ", " ").trim();
```

### Using String.replaceAll and String.trim

The following code snippet can be used to replace 2 or more spaces with single space in string and delete leading and trailing spaces using String.replaceAll and String.trim:

```
String str = "   This is a   string   with   multiple   spaces   ";
str = str.replaceAll("  ", " ").trim();
```

### Using StringUtils.replace and StringUtils.trim

The following code snippet can be used to replace 2 or more spaces with single space in string and delete leading and trailing spaces using StringUtils.replace and StringUtils.trim:

```
String str = "   This is a   string   with   multiple   spaces   ";
str = StringUtils.replace(str, "  ", " ").trim();
```
