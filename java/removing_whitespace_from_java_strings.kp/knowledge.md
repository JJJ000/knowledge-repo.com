---
title: Remove all leading and trailing whitespace from a Java string
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the trim() method to remove leading and trailing spaces from a Java String.
---

**Contents**

[TOC]

## String.trim()

The `String.trim()` method removes leading and trailing spaces from a given string. It returns a new string with the whitespace removed, leaving all other characters in the original string intact.

## Syntax

The syntax for `String.trim()` is as follows:

```
String str = "  Hello World  ";
String strTrimmed = str.trim();
```

## Example

The following example shows how `String.trim()` can be used to remove leading and trailing spaces from a string:

```
String str = "  Hello World  ";
String strTrimmed = str.trim();
System.out.println(strTrimmed); // Outputs "Hello World"
```

## Output

The output of the above code is:

```
Hello World
```
