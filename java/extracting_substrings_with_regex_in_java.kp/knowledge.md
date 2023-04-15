---
title: What is the syntax for extracting a substring using regular expressions?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the String.matches() or String.replaceAll() methods to extract a substring using regex in Java.
---

**Contents**

[TOC]

### Create Regex

The first step is to create the regex pattern that will be used to extract the substring. This can be done by using the `Pattern` class in Java. For example, to create a regex pattern that extracts a substring between two words, the following code can be used:

```java
Pattern pattern = Pattern.compile("\\w+(?=\\sword2)\\sword2");
```

### Create Matcher

Once the regex pattern is created, it can be used to create a `Matcher` object. This can be done by using the `Matcher` class and passing in the regex pattern as an argument. For example:

```java
Matcher matcher = pattern.matcher("string to search");
```

### Find Substring

The `Matcher` object can then be used to find the substring. This can be done by using the `matcher.find()` method, which will return `true` if the substring is found and `false` otherwise.

### Extract Substring

Once the substring is found, it can be extracted by using the `matcher.group()` method. This will return the substring that was found by the regex pattern.
