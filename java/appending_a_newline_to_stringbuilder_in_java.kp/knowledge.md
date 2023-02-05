---
title: How to add a new line to stringbuilder
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: StringBuilder can be appended with a newline character using the append(`\n`) method.
---

**Contents**

[TOC]

# Section 1: Overview
StringBuilder is a class in Java that is used to construct strings from pieces. It is a mutable sequence of characters and is similar to the String class, but it can be modified.

# Section 2: Appending a Newline
A newline can be appended to a StringBuilder object by calling the append() method and passing a newline character as an argument. The newline character can be represented by the "\n" escape sequence or the System.lineSeparator() method.

# Section 3: Example
For example, the following code snippet appends a newline to a StringBuilder object:

```
StringBuilder sb = new StringBuilder();
sb.append("This is a line of text");
sb.append(System.lineSeparator());
```

# Section 4: Conclusion
By using the append() method and passing a newline character as an argument, it is possible to append a newline to a StringBuilder object. This can be done using either the "\n" escape sequence or the System.lineSeparator() method.
