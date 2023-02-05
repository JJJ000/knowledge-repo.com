---
title: Breaking apart a string using the pipe symbol ("|")
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The String class has a split() method which can be used to split a string into an array of substrings using a given delimiter, such as the pipe character `|`.
---

**Contents**

[TOC]

### Using the `split()` Method

The `split()` method of the `String` class can be used to split a string by a specified delimiter. In this case, the delimiter is the pipe character (`|`).

```java
String str = "Hello|World";
String[] splittedString = str.split("\\|");
```

The `split()` method returns an array of `String` objects, each containing a part of the original string.

### Using the `Pattern` Class

The `Pattern` class provides a more powerful way to split a string. It allows for more complex regular expressions to be used as the delimiter.

```java
String str = "Hello|World";
Pattern pattern = Pattern.compile("\\|");
String[] splittedString = pattern.split(str);
```

### Using the `StringTokenizer` Class

The `StringTokenizer` class is another way to split a string. It is simpler than the `Pattern` class, and allows for a single delimiter to be specified.

```java
String str = "Hello|World";
StringTokenizer tokenizer = new StringTokenizer(str, "|");
```

The `StringTokenizer` class returns a `StringTokenizer` object, which contains a list of the tokens. The tokens can be retrieved using the `nextToken()` method.

### Using the `String.split()` Method with a Regular Expression

The `String.split()` method can also be used with a regular expression as the delimiter. This allows for more complex patterns to be used as the delimiter.

```java
String str = "Hello|World";
String[] splittedString = str.split("\\|");
```

The `split()` method returns an array of `String` objects, each containing a part of the original string.
