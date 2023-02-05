---
title: What is the suggested method for encoding html characters in plain java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The recommended way to escape HTML symbols in plain Java is to use the StringEscapeUtils.escapeHtml4() method from the Apache Commons Lang library.
---

**Contents**

[TOC]

## HTML Character Entities

HTML character entities are used to represent special characters in HTML documents. These entities are preceded by an ampersand (&) and a pound sign (#), and are followed by a semicolon (;). For example, the HTML entity for the less-than sign (<) is &lt;.

## Java Escape Sequences

Java escape sequences are used to represent special characters in Java strings. These sequences are preceded by a backslash (\). For example, the Java escape sequence for the less-than sign (<) is \u003c.

## Using Java's StringEscapeUtils

Java's StringEscapeUtils class provides a convenient way to escape HTML symbols in plain Java. The escapeHtml() method of this class takes a String as an argument and returns a String with HTML symbols replaced with their corresponding HTML entities.

## Using Apache Commons Lang's StringEscapeUtils

Apache Commons Lang's StringEscapeUtils class also provides a convenient way to escape HTML symbols in plain Java. The escapeHtml4() method of this class takes a String as an argument and returns a String with HTML symbols replaced with their corresponding HTML entities.
