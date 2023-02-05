---
title: What is the distinction between java.lang.runtimeexception and java.lang.exception?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: RuntimeException is an unchecked exception, meaning it does not need to be caught, whereas Exception is a checked exception, meaning it must be caught.
---

**Contents**

[TOC]

# RuntimeException
RuntimeException is a type of exception that is thrown when an application is running and an unexpected condition occurs. It is an unchecked exception and does not need to be declared in a method or constructor's throws clause.

# Exception
Exception is a type of exception that is thrown when a program is running and an unexpected condition occurs. It is a checked exception and must be declared in a method or constructor's throws clause.
