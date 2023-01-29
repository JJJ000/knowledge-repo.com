---
title: What is the correct syntax for including a percent sign in a string.format?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use two percentage symbols (%%), which will be interpreted as a single percent sign.
---

**Contents**

[TOC]

### Escaping with Backslash

The simplest way to escape a percent sign in Java is to use a backslash (\). This can be done in a `String.format()` statement by adding a backslash before the percent sign. For example:

```
String result = String.format("This is a percentage sign: \%");
```

### Using the Percent Character Code

Another way to escape a percent sign in Java is to use the character code for the percent sign, which is `%25`. This can be done in a `String.format()` statement by adding the character code instead of the percent sign. For example:

```
String result = String.format("This is a percentage sign: %25");
```

### Escaping with Double Backslash

A third way to escape a percent sign in Java is to use a double backslash (\\%). This can be done in a `String.format()` statement by adding two backslashes before the percent sign. For example:

```
String result = String.format("This is a percentage sign: \\%");
```

### Using the Unicode Character Code

A fourth way to escape a percent sign in Java is to use the Unicode character code for the percent sign, which is `\u0025`. This can be done in a `String.format()` statement by adding the Unicode character code instead of the percent sign. For example:

```
String result = String.format("This is a percentage sign: \u0025");
```
