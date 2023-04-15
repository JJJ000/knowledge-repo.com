---
title: What is the process for transforming a string into a charsequence?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the CharSequence constructor with the String as an argument to convert a String to CharSequence.
---

**Contents**

[TOC]

`**` What is a CharSequence?**

A CharSequence is an interface in the Java programming language that represents a sequence of characters. It is a read-only interface, meaning that the characters cannot be modified once they are created.

`**` What is a String?**

A String is a sequence of characters in the Java programming language, represented by the String class. A String is a type of CharSequence, meaning that it can be used wherever a CharSequence is required.

`**` How to Convert a String to CharSequence**

Since a String is already a type of CharSequence, it does not need to be explicitly converted. To use a String as a CharSequence, simply pass the String as an argument to the method that requires a CharSequence.

`**` Examples of Converting a String to CharSequence**

The following example shows how to convert a String to a CharSequence:

String str = "Hello World!";
CharSequence cs = str; // No explicit conversion needed
