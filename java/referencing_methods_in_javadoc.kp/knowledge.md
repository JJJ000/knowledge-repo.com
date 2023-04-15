---
title: What is the proper syntax for referencing a method in javadoc?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: In Javadoc, a method should be referenced by its fully qualified name, including the class name and method signature.
---

**Contents**

[TOC]

### Syntax

The syntax for referencing a method in javadoc is as follows:

`@see <fully qualified class name>#<method name>(<parameter list>)`

### Parameters

* `<fully qualified class name>` - The fully qualified name of the class containing the method.
* `<method name>` - The name of the method.
* `<parameter list>` - The list of parameters for the method.

### Example

For example, if we wanted to reference the `toString()` method in the `java.lang.Object` class, we would use the following syntax:

`@see java.lang.Object#toString()`
