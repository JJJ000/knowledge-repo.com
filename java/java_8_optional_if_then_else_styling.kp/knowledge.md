---
title: What are the functional capabilities of Java 8's optional.ifpresent and optional.ifnotpresent?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The functional style of Java 8`s Optional.ifPresent is to execute the given action if a value is present, and the functional style of the if-not-Present is to execute the given action if a value is not present.
---

**Contents**

[TOC]

### ifPresent

`Optional.ifPresent` is a functional-style method that takes a `Consumer` as an argument. The `Consumer` is a functional interface that takes an argument and performs a task with it. The `Optional.ifPresent` method will evaluate the `Optional` and, if it has a value, it will pass that value to the `Consumer` for execution.

### ifNotPresent

`Optional.ifNotPresent` is a functional-style method that takes a `Runnable` as an argument. The `Runnable` is a functional interface that takes no arguments and performs a task. The `Optional.ifNotPresent` method will evaluate the `Optional` and, if it is empty, it will execute the `Runnable`.
