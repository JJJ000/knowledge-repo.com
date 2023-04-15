---
title: Is there a way to create multiline strings in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, Java supports multiline strings using the triple-quote syntax.
---

**Contents**

[TOC]

### Yes
Java does support multiline strings. Multiline strings in Java are represented using triple quotes, i.e. `"""`.

### Syntax
The syntax for creating multiline strings in Java is as follows:

```
String multiLineString = """
line1
line2
line3
""";
```

### Usage
Multiline strings can be used in Java to store multiple lines of text in a single string. This is useful for storing large amounts of text such as code snippets, JSON objects, HTML, etc.

### Example
Here is an example of a multiline string in Java:

```
String html = """
<html>
  <head>
    <title>My Page</title>
  </head>
  <body>
    <h1>Welcome to my page!</h1>
  </body>
</html>
""";
```
