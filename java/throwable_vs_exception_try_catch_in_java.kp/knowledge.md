---
title: What is the distinction between throwing a throwable and an exception in a try-catch block?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Throwable is the parent class of Exception, so Exception is more specific and should be used unless there is a need to catch a broader range of errors.
---

**Contents**

[TOC]

### Throwable
Throwable is the superclass of all errors and exceptions in the Java language. It is the base class of all errors and exceptions in the Java language and is the parent class of all exceptions and errors.

### Exception
Exception is a subclass of Throwable that indicates conditions that a reasonable application might want to catch. It is used to indicate that a problem occurred, but it is not a serious system error. It is used to indicate conditions that a reasonable application might want to catch.

### Difference
The main difference between Throwable and Exception is that Throwable is the parent class of all errors and exceptions in the Java language, while Exception is a subclass of Throwable that indicates conditions that a reasonable application might want to catch. Throwable can be used to catch all errors and exceptions, while Exception should be used to catch only those exceptions that a reasonable application might want to catch.
