---
title: How do canonical name, simple name, and class name differ in a Java class?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The canonical name is the fully qualified name of a class, the simple name is the class name without the package name, and the class name is the name of the class including the package name.
---

**Contents**

[TOC]

### Canonical Name
The canonical name of a class is the fully qualified name of the class, including the package name. It is the name used when loading the class with the Class.forName() method.

### Simple Name
The simple name of a class is the class name without the package name. It is the name used when you are referring to the class within its own package.

### Class Name
The class name is the same as the simple name. It is the name used when you are creating an instance of the class.
