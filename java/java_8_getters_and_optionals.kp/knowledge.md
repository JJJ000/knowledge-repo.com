---
title: Should the return values of Java 8 getters be of an optional type?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: No, Java 8 getters should not return optional type.
---

**Contents**

[TOC]

### Pros

- Optional types can be used to represent the absence of a value and indicate that a field may not be present. This can be useful when dealing with data that may be missing or incomplete.

- Optional types provide a way to explicitly handle the absence of a value, which can prevent errors caused by accessing a null value.

- Optional types can provide useful information about the state of a value, such as whether or not it is present.

### Cons

- Optional types can make code more verbose and difficult to read, as the code must be written to explicitly handle the case where a value is absent.

- Optional types can be difficult to use correctly, as they require the programmer to remember to check for the presence of a value before attempting to access it.

- Optional types can be difficult to debug, as errors caused by accessing a null value may not be immediately apparent.
