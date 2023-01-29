---
title: What is the reason junit does not offer assertnotequals methods?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: JUnit does provide assertNotEquals methods in Java, however, they are deprecated in favor of the assertNotSame and assertNotEquals methods.
---

**Contents**

[TOC]

### Assert vs AssertEquals
JUnit provides two types of assertion methods: assert and assertEquals. The assert method is used to test a boolean expression, while assertEquals is used to compare two values for equality.

### Why No assertNotEquals
The assertEquals method is designed to compare two values for equality, and so it does not make sense to have an assertNotEquals method. To test for inequality, the assert method can be used instead. The assert method allows for a boolean expression to be tested, which can be used to test for inequality.
