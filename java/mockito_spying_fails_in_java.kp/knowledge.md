---
title: Attempting to spy on a method using mockito will cause the original method to be invoked
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: No, spying on a method does not call the original method in Java.
---

**Contents**

[TOC]

####Yes
When trying to spy on a method, Mockito will call the original method. This means that any changes that the original method may make will still take place. This can be useful for testing the behaviour of the original method, but can also lead to unexpected behaviour if the original method is not expected to be called.

####No
Mockito also provides the ability to stub out the original method, so that it does not get called. This can be useful if the original method is not expected to be called, or if the behaviour of the original method needs to be changed in a test. By stubbing out the original method, the behaviour of the method can be controlled in the test.
