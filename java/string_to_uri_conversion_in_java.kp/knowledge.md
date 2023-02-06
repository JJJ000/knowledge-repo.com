---
title: Transform string into uri
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The Uri class can be used to convert a String to a Uri in Java.
---

**Contents**

[TOC]

# Section 1: Overview
A URI (Uniform Resource Identifier) is a string of characters used to identify a resource. In Java, the `java.net.URI` class provides methods to convert a String to a URI.

# Section 2: Creating a URI
To create a URI from a String, you can use the `URI` class' constructor. The constructor takes a String as an argument and parses it into a `URI` object.

# Section 3: Validating a URI
Before creating a `URI` from a String, it is important to make sure the String is valid. The `URI` class provides the `validate()` method to validate a String before creating a `URI` from it.

# Section 4: Examples
Here are some examples of creating a `URI` from a String:

```java
String str = "http://example.com";
URI uri = new URI(str);

String str2 = "ftp://user:password@example.com/files";
URI uri2 = new URI(str2);
```
