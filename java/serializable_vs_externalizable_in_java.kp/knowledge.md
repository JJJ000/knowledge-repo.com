---
title: How do serializable and externalizable in Java differ?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Serializable is a marker interface that allows an object to be serialized, while Externalizable is an interface that allows a class to control the serialization process.
---

**Contents**

[TOC]

### Serializable
Serializable is a marker interface that marks a class as being serializable. It is used to persist the state of an object by converting it to a byte stream. It has no methods or fields and is implemented by all of the wrapper classes, such as Integer, Boolean, etc.

### Externalizable
Externalizable is a sub-interface of Serializable and is used to give control over the serialization process to the developer. It has two methods, readExternal() and writeExternal(), that the developer must implement in order to control the serialization process. It provides more flexibility than Serializable, but requires more work to implement.
