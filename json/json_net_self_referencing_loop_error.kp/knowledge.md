---
title: A self-referencing loop was detected while using json.net for the given type
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Self-referencing loops in JSON can cause infinite recursion and result in a stack overflow exception.
---

**Contents**

[TOC]

# Overview

JSON.NET is a popular library for serializing and deserializing .NET objects into JSON data. It is used in many applications to allow for easy data exchange between different systems. However, when serializing and deserializing complex object graphs, it can sometimes throw an error due to a self-referencing loop.

# What is a Self-Referencing Loop?

A self-referencing loop occurs when an object references itself, either directly or indirectly. This can lead to an infinite loop when the object is serialized or deserialized. For example, consider the following object graph: 

```
class A
{
    public B b;
}

class B
{
    public A a;
}
```

In this example, class A contains a reference to an instance of class B, and class B contains a reference to an instance of class A. This creates a self-referencing loop, which can cause issues when serializing or deserializing the object graph.

# How Does JSON.NET Handle Self-Referencing Loops?

JSON.NET is designed to detect self-referencing loops and throw an exception when they are encountered. This prevents the serializer from getting stuck in an infinite loop when attempting to serialize or deserialize the object graph. The exception thrown is a JsonSerializationException with the message “Self referencing loop detected for type ‘{type}’”.

# Conclusion

Self-referencing loops can be a common issue when serializing and deserializing complex object graphs. JSON.NET is designed to detect these loops and throw an exception when they are encountered. This allows developers to quickly identify and fix any issues with their object graphs.
