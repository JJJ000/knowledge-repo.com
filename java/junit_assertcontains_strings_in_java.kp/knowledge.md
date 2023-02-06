---
title: Testing if a string contains a certain value using assertcontains in junit
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: jUnit provides the assertContains() method which can be used to check if a string contains a specified substring.
---

**Contents**

[TOC]

### Using AssertContains

The `AssertContains` method is used to check if a string contains a given substring. It is part of the `org.junit.Assert` class.

### Syntax

The syntax for the `AssertContains` method is as follows:

```java
static void assertContains(String message, String substring, String string)
```

The `message` parameter is an optional message that is displayed if the assertion fails. The `substring` parameter is the substring that is being searched for within the `string` parameter.

### Example

The following example shows how to use the `AssertContains` method to check if the string "Hello World" contains the substring "World":

```java
String string = "Hello World";
String substring = "World";

assertContains("The string does not contain the substring", substring, string);
```

If the assertion fails, the following message will be displayed:

`The string does not contain the substring`
