---
title: What is the distinction between doreturn() and when() in mockito?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: doReturn() is used to stub a method call and when() is used to set expectations on a method call.
---

**Contents**

[TOC]

### doReturn()
`doReturn()` is used when you want to stub a void method with a return value. It is used when you want to stub a method without affecting the real method of the class.

### when()
`when()` is used to stub a method which has a return type. It is used to define the behavior of a mocked method to return a specific value. It also affects the real method of the class.
