---
title: Intellij's inspection feature highlights an "unresolved symbol" error, although the code still compiles successfully
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: IntelliJ inspection is a static analysis tool and will not detect any errors that only occur at runtime, so it is possible for code to compile despite IntelliJ giving a `Cannot resolve symbol` error.
---

**Contents**

[TOC]

### Overview
IntelliJ is an integrated development environment (IDE) used to develop Java applications. It provides an editor and compiler that can detect errors in code. One of the errors it can detect is a "Cannot resolve symbol" error, which occurs when the compiler is unable to find the symbol referenced in the code. Despite this error, the code may still compile and run without issue.

### Causes of the Error
The "Cannot resolve symbol" error is usually caused by a typo or a missing import statement. The compiler is unable to find the symbol in the code because it is not defined or imported. For example, if a variable is used in the code but not declared, the compiler will not be able to find the symbol and will display the error.

### Implications
While the code may still compile and run without issue, the "Cannot resolve symbol" error should not be ignored. The error indicates that the code is not well-structured and may lead to unexpected errors in the future. It is important to address these errors as soon as possible to ensure that the code is robust and reliable.

### Solution
The best way to address the "Cannot resolve symbol" error is to double-check the code for typos and missing import statements. If a symbol is used in the code but not declared or imported, it should be declared or imported. This will ensure that the compiler can find the symbol and the error will be resolved.
