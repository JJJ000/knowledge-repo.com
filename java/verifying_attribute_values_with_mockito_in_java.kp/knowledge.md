---
title: Check the value of an object's attribute using mockito
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Mockito can be used to verify that an object`s attributes have the expected values.
---

**Contents**

[TOC]

### Overview
Mockito is a popular mocking framework for Java. It allows developers to create mock objects for testing purposes. Mockito can be used to verify object attribute values in Java. This can be done by using Mockito's `verify` method.

### Setting Up Mockito
In order to use Mockito to verify object attribute values, the first step is to set up Mockito. This can be done by adding the Mockito dependency to the project's `pom.xml` file.

### Verifying Object Attribute Values
Once Mockito is set up, developers can use the `verify` method to verify object attribute values. This is done by passing the object to verify and the attribute name to the `verify` method. The `verify` method will then check the object's attribute value and return a boolean value indicating whether it matches the expected value.

### Example
For example, consider the following code snippet:

```java
Object obj = new Object();
obj.setAttribute("value");

boolean result = Mockito.verify(obj, "attribute", "value");
```

In this example, the `verify` method will check the value of the `attribute` attribute on the `obj` object. If the value matches the expected value of "value", the `verify` method will return `true`. Otherwise, it will return `false`.
