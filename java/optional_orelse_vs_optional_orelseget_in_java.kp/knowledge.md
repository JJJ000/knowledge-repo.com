---
title: What is the distinction between "optional.orelse()" and "optional.orelseget()"?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Optional.orElse() returns a default value if the Optional is empty, while Optional.orElseGet() returns the result of a Supplier if the Optional is empty.
---

**Contents**

[TOC]

### Optional.orElse()
`Optional.orElse()` is a method that takes an argument and returns the value of the Optional if present, otherwise returns the argument.

### Optional.orElseGet()
`Optional.orElseGet()` is a method that takes a Supplier as an argument and returns the value of the Optional if present, otherwise returns the result of invoking the Supplier.

### Difference
The main difference between `Optional.orElse()` and `Optional.orElseGet()` is that `orElse()` takes an argument and returns it if the Optional is empty, while `orElseGet()` takes a Supplier as an argument and returns the result of invoking the Supplier if the Optional is empty. This means that `orElseGet()` is more efficient as it only evaluates the Supplier if the Optional is empty, whereas `orElse()` always evaluates the argument.
