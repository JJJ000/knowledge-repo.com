---
title: How do class.getresource() and classloader.getresource() differ?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Class.getResource() looks for resources relative to the class path, while ClassLoader.getResource() looks for resources relative to the class loader`s path.
---

**Contents**

[TOC]

### Class.getResource()
Class.getResource() is a method that is used to locate a resource by the given name using the same classloader that loaded the class. It searches for the resource in the same package as the class and returns the URL object representing the resource.

### ClassLoader.getResource()
ClassLoader.getResource() is a method used to locate a resource by the given name using the classloader that loaded the class. It searches for the resource in the whole classpath and returns the URL object representing the resource.

### Difference
The main difference between Class.getResource() and ClassLoader.getResource() is that Class.getResource() searches for the resource in the same package as the class, whereas ClassLoader.getResource() searches for the resource in the whole classpath.
