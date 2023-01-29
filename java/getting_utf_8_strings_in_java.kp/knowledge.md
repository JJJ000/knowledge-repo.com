---
title: What is the syntax for creating a "utf-8" string literal in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: UTF-8 string literals can be created in Java using the String constructor with the UTF-8 encoding parameter.
---

**Contents**

[TOC]

### Java Source Code

Java source code can be used to create UTF-8 string literals. This can be done by using the Unicode escape sequence `\uXXXX`, where `XXXX` is a four digit hexadecimal code for the desired character. For example, the Unicode escape sequence `\u00A9` creates the copyright symbol.

### Java String Literal

Java string literals can also be used to create UTF-8 strings. This is done by simply writing the desired characters within double quotes. For example, the string literal `"©"` creates the copyright symbol.

### Java Resource Bundle

Java resource bundles can also be used to create UTF-8 strings. This is done by loading the desired characters into a resource bundle and then referencing them in the code. For example, the resource bundle can contain the string `"©"` and then be referenced in the code to create the copyright symbol.

### Java Internationalization

Java internationalization can also be used to create UTF-8 strings. This is done by using the `ResourceBundle` class to load the desired characters from a resource bundle and then referencing them in the code. For example, the resource bundle can contain the string `"©"` and then be referenced in the code to create the copyright symbol.
