---
title: The difference between a final and an effectively final variable is that a final variable must be explicitly declared as final, while an effectively final variable is a variable that is not declared as final but is not modified after it is initialized
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A final variable is declared with the keyword `final`, while an effectively final variable is not declared with the keyword `final`, but is never changed after it is initialized.
---

**Contents**

[TOC]

### Final

In Java, the keyword `final` is used to declare a variable, method, or class as unmodifiable. For example, a `final` variable can only be assigned a value once, and any attempt to reassign a value will throw a compile-time error.

### Effectively Final

In Java, a variable is considered to be "effectively final" if it is not explicitly declared as `final`, but its value is never changed after it is initially assigned. This is a concept used in the context of lambda expressions and anonymous classes, where variables from the enclosing scope can be used in the inner scope without explicitly declaring them as `final`.
