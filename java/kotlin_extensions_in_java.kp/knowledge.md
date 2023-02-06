---
title: Calling kotlin extension functions from java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Kotlin extension functions can be accessed from Java by using the fully qualified name of the function.
---

**Contents**

[TOC]

### Section 1: Overview
Kotlin extension functions are a powerful tool for extending the functionality of existing classes without having to inherit from them. They allow you to add functionality to existing classes without having to modify the existing code. This can be especially useful when working with third-party libraries.

### Section 2: Accessing Kotlin Extension Functions from Java
Kotlin extension functions can be accessed from Java code by using the `@JvmName` annotation. This annotation allows you to specify the name of the function in the Java code. For example, if you have a Kotlin extension function named `foo()`, you can access it from Java code using the annotation `@JvmName("foo")`.

### Section 3: Benefits of Using Kotlin Extension Functions
Using Kotlin extension functions from Java code has several benefits. First, it allows you to extend the functionality of existing classes without having to modify the existing code. Second, it can help reduce the amount of boilerplate code needed to access the functionality of the extension function. Finally, it can help reduce the amount of time needed to develop and maintain the code.

### Section 4: Conclusion
Kotlin extension functions are a powerful tool for extending the functionality of existing classes without having to modify the existing code. They can be accessed from Java code by using the `@JvmName` annotation. Using Kotlin extension functions from Java code can help reduce the amount of boilerplate code needed and can help reduce the amount of time needed for development and maintenance.
