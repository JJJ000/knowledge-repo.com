---
title: Jackson's serializer and deserializer
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Serializing is the process of converting an object into a stream of bytes in order to store the object or transmit it to memory, while Deserializing is the process of converting the stream of bytes back into an object.
---

**Contents**

[TOC]

## Serializing
Serializing is the process of converting an object into a stream of bytes in order to store the object or transmit it to memory, a database, or a file. Its main purpose is to save the state of an object in order to be able to recreate it when needed. In Java, serialization is done by implementing the Serializable interface.

## Deserializing
Deserializing is the reverse process of creating an object from a stream of bytes. It is used to convert the serialized form of an object back into a copy of the object. In Java, deserialization is done by using the ObjectInputStream class.

## Jackson
Jackson is a popular library for handling JSON in Java. It can be used for both serializing and deserializing JSON. It provides a high-level facade for processing JSON, as well as the ability to work with JSON as an object model in its own right. Jackson also provides a number of powerful data binding capabilities.
