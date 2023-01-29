---
title: Distinguishing between checked and unchecked exceptions in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Unchecked exceptions are not checked at compile-time, while checked exceptions must be either caught or declared in a throws clause.
---

**Contents**

[TOC]

### Checked Exceptions
Checked exceptions are exceptions that are checked at compile time. These are exceptions that are expected to be handled by the code. If the code does not handle these exceptions, the compiler will not compile the code and will throw an error. Examples of checked exceptions include IOException, SQLException, FileNotFoundException, etc.

### Unchecked Exceptions
Unchecked exceptions are exceptions that are not checked at compile time. These are exceptions that are not expected to be handled by the code. The compiler will not throw an error if the code does not handle these exceptions. Examples of unchecked exceptions include NullPointerException, ArrayIndexOutOfBoundsException, etc.
