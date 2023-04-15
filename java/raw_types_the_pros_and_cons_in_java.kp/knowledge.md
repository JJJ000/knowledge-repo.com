---
title: What are the disadvantages of using a raw type, and why should it be avoided?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A raw type is a generic type that has been declared without any type parameters, and should not be used in Java as it can lead to unexpected runtime exceptions.
---

**Contents**

[TOC]

####What is a Raw Type?
A raw type is a generic type without any type parameters. Raw types were introduced in Java 5 to maintain backwards compatibility with non-generic code. 

####Why Shouldn't We Use Raw Types?
Raw types should not be used because they can lead to unexpected behavior. Since raw types do not have any type parameters, the compiler does not perform type checking, which can lead to ClassCastExceptions at runtime. Additionally, raw types can lead to unchecked warnings, which indicate that the code may not be type safe.
