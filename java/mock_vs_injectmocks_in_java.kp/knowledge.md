---
title: What is the distinction between @mock and @injectmocks?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: @Mock is used to create mock objects, while @InjectMocks is used to inject mock objects into the class under test.
---

**Contents**

[TOC]

1. **@Mock**
   - @Mock annotation is used in Mockito to create and inject mocked instances.
   - It can be used on a field or local variable in order to create a mock instance of the corresponding type.
   - The mock instance is then used to stub methods or verify behavior during a unit test.

2. **@InjectMocks**
   - @InjectMocks annotation is used in Mockito to inject mocked dependencies into a class.
   - It can be used on a field or local variable in order to inject the mocked dependencies into the class.
   - The mocked dependencies are then used to stub methods or verify behavior during a unit test.
