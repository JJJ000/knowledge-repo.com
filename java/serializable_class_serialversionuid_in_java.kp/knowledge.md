---
title: What is the purpose of a static final serialversionuid field in a serializable class?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: A serializable class in Java that does not declare a static final serialVersionUID field will be assigned a default serialVersionUID value by the compiler.
---

**Contents**

[TOC]

# What is Serializable
Serializable is an interface in Java that allows objects to be converted into a stream of bytes that can be saved to a file or sent over a network. It is used to store objects so that they can be retrieved at a later time.

# What is SerialVersionUID
SerialVersionUID is a unique identifier for a serializable class. It is used to verify that the class is compatible with the stream of bytes that it is being deserialized from. If the class does not declare a static final serialVersionUID field, the serialization runtime will generate a default serialVersionUID value for that class.

# What Does it Mean
When a serializable class does not declare a static final serialVersionUID field, it means that the serialization runtime will generate a default serialVersionUID value for the class. This value will be used to verify that the class is compatible with the stream of bytes that it is being deserialized from. If the class is not compatible, an InvalidClassException will be thrown.
