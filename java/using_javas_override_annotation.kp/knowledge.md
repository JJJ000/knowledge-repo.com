---
title: What is the purpose of using java's @override annotation and when should it be applied?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: @Override is used when overriding a method from a superclass to ensure that the method signature is correct.
---

**Contents**

[TOC]

### Definition
The @Override annotation is used to indicate that a method is overriding a method of a superclass or implementing a method of an interface.

### Usage
The @Override annotation is used when a method is being overridden from a superclass or implemented from an interface. This annotation is used to ensure that the overriding or implementing method has the correct signature and is not a new method. It also helps to make the code more readable and maintainable.

### Benefits
Using the @Override annotation provides several benefits. It helps to ensure that the correct method is being overridden or implemented, which helps to prevent errors. It also helps to make the code more readable and maintainable by making it clear which methods are being overridden or implemented.

### Caveats
The @Override annotation should not be used when a method is not overriding or implementing a method. Doing so can lead to errors and unexpected behavior. Additionally, the annotation should only be used when the method is being overridden or implemented from a superclass or interface. If the method is being overridden or implemented from a different source, the annotation should not be used.
