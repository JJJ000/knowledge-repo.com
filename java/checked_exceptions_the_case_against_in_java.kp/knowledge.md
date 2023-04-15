---
title: An argument against using checked exceptions
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Checked exceptions can lead to code that is more verbose and difficult to read.
---

**Contents**

[TOC]

### Unnecessary Complexity
Checked exceptions add unnecessary complexity to the Java language. Since they must be declared when they are thrown, they require more code than unchecked exceptions. This can lead to a lot of boilerplate code, which can be difficult to read and maintain. In addition, checked exceptions can lead to a "catch-all" mentality, where developers try to catch all possible exceptions in order to avoid compilation errors. This can lead to code that is difficult to debug and maintain.

### Poor Error Handling
Checked exceptions can lead to poor error handling. Since they must be declared when they are thrown, developers may be tempted to simply "swallow" the exception instead of properly handling it. This can lead to unexpected errors and difficult to debug issues.

### Not Suitable for All Situations
Checked exceptions are not suitable for all situations. For example, they may not be suitable for asynchronous operations, where the exact exception type is not known in advance. In these cases, developers must catch all possible exceptions, which can lead to code that is difficult to maintain.

### Unnecessary Overhead
Checked exceptions can add unnecessary overhead to the code. Since they must be declared when they are thrown, they require more code than unchecked exceptions. This can lead to increased compile times and slower program execution.
